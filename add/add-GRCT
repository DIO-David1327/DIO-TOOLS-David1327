// ==UserScript==
// @name         add GRCT
// @version      2024-10-30
// @description  add GRCT
// @author       David1327
// @icon         data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==
// @grant        none
// ==/UserScript==


/*******************************************************************************************************************************
     * autre
     *******************************************************************************************************************************/

    function filldiomenu() {
        if ($('#dio_mnu_list').length == 0) {
            $('<style id="dio__style"> ' +
                '.dio {background: url(' + Home_url + '/img/dio/logo/layout_3.3.0.png) -4px -80px no-repeat;}' +
                '#dio_mnu_list ul { height: auto !important;}' +
                '#dio_mnu_list li { width: 125px !important;}' +
                '#dio_mnu { background: url(' + Home_url + '/img/dio/logo/layout_3.3.0.png) no-repeat; width: 142px; height: 75px;}' +
                '#dio_mnu .btn_settings.circle_button {top: 34px; right: 55px;}' +
                '#dio_mnu .dio_icon { height: 24px; width: 24px; margin: 7px 0px 0px 4px; }' +
                '.icon.dio_icon { margin-left: -2px; }' +
                '#grcrt_mnu .btn_settings { right: 0px!important; position: relative; }' +
                '.dio.abh { background-position: -42px -80px; }' +
                '.dio.aom { background: url(https://gpfr.innogamescdn.com/images/game/academy/points_25x25.png) no-repeat; top: 4px !important; left: 4px !important; }' +
                '#dio_mnu_list .icon.Notification { background: url("https://dio-david1327.github.io/img/dio/btn/subforum-old.png") no-repeat; margin: 2px; }' +
                '</style>').appendTo('head');
            $('#ui_box').append($('<img/>', { 'src': 'https://dio-david1327.github.io/img/dio/logo/icon.gif', 'id': 'grcgrc', 'style': 'position:absolute;bottom:0px;left:0px;z-index:1000' }));
            $('#ui_box div.bottom_ornament').before($('<div/>', { 'id': 'dio_mnu_list', 'class': "container_hidden", 'style': "position: absolute;right: -10px;bottom: 6px;"/*position:relative;"*/ })
                .append($('<div/>', { 'class': "top" })).append($('<div/>', { 'class': "bottom" }))
                .append($('<div/>', { 'class': "middle nui_main_menu", 'style': 'top: 0px; width: 142px;' })
                    .append($('<div/>', { 'class': "left" }))
                    .append($('<div/>', { 'class': "right", 'style': 'z-index:10;' }))
                    .append($('<div/>', { 'class': "content", 'style': "display:none; margin-top: 0; margin-bottom: 0;" }).append($('<div/>', { 'class': "units_wrapper clearfix" }).append($('<ul/>'))))
                )
            )
            $('#ui_box div.bottom_ornament')
                .append($('<div/>', { 'id': 'dio_mnu' })
                    .append($('<div/>', { 'class': "btn_settings circle_button", 'style': '' })
                        .append($('<div/>', { 'class': "dio_icon js-caption", 'style': '' }))
                        .mousePopup(new uw.MousePopup(""))
                        .click(function () {
                            $('#dio_mnu_list li.main_menu_item').remove()
                            if ($('#dio_mnu>div.btn_settings').hasClass('active checked')) {
                                $('#dio_mnu_list .content').slideUp(500, function () { $('#dio_mnu_list').animate({ right: -10 }, 300) })
                            } else {
                                $('.btn_gods_spells').hasClass('active') && $('.btn_gods_spells').click()
                                $('#dio_mnu_list').animate({ right: 134 }, 300, function () { $('#dio_mnu_list .content').slideDown(500) })
                            }
                            $('#dio_mnu>div.btn_settings').toggleClass('active checked')
                            // $('#dio_mnu_list').slideToggle(),
                        })
                    )
                )
            $('#dio_mnu_list>.bottom').css({
                'background': $('.gods_spells_menu>.bottom').css('background'),
                'height': $('.gods_spells_menu>.bottom').css('height'),
                'position': $('.gods_spells_menu>.bottom').css('position'),
                'bottom': '-27px'
            });
        }
        setTimeout(() => {
            $('#dio_dio-grct_style').remove();
            if ($('#grcrt_mnu').length) {
                $('<style id="dio_dio-grct_style">' +
                    '#grcrt_mnu {display: contents;}' +
                    '#grcrt_mnu .btn_settings.circle_button {top: -41px!important; right: 21px!important;}' +
                    '#dio_mnu .btn_settings.circle_button {top: 6px; right: 37px;}' +
                    '#dio_mnu { background: url(' + Home_url + '/img/dio/logo/dio-grct.png) no-repeat; width: 142px; height: 47px;}' +
                    '</style>').appendTo('head');
            };
        }, 2000);

        $('#dio_mnu_list ul li').remove()
        $.each(dio.menu, function (indM, eleM) {
            $('#dio_mnu_list ul').append(
                $('<li/>').append(
                    $('<span/>', { 'class': "content_wrapper" }).append(
                        $('<span/>', { 'class': "button_wrapper" }).append(
                            $('<span/>', { 'class': "button" }).append(
                                $('<span/>', { 'class': "icon dio" + (eleM.class ? " " + eleM.class : "") })
                            ).append(
                                $('<span/>', { 'class': "indicator", 'style': "display: none;" })
                            )
                        ).append(
                            $('<span/>', { 'class': "name_wrapper", 'style': 'width: 90px; height: 34px;' }).append(
                                $('<span/>', { 'class': "name" }).html(eleM.name) //RepConvTool.GetLabel(eleM.name)
                            )
                        )
                    )
                ).click(function () {
                    eval(eleM.action);
                }).attr('id', eleM.id)
            );
        });
        $('#dio_mnu_list .Notification').tooltip(getTexts("Settings", "Update") + " " + dio_version + " / " + getTexts("labels", "donat") + " / " + getTexts("translations", "translations") + " / BUG");
    }
    dio.menu[6] = { 'name': getTexts("hotkeys", "settings"), 'action': 'openSettings()', 'class': 'dio_icon ' }
    dio.menu[5] = { 'name': getTexts("tutoriel", "tuto"), 'action': 'Notification.activate();', 'class': 'dio_icon Notification' }
    filldiomenu()


    "undefined" == typeof Object.size && (Object.size = function (g) {
        var A = 0, d;
        for (d in g) { g.hasOwnProperty(d) && A++; }
        return A;
    });

    "undefined" == typeof Array.prototype.contains && (Array.prototype.contains = function (g) {
        for (var A = this.length; A--;) if (this[A] == g) return !0;
        return !1;
    });

    dio.AddBtn = function (pId, pWndName) {
        var
            //WndName = (typeof pWndName != 'undefined') ? pWndName : '',
            WndName = pWndName || '',
            _btn = $('<div/>', {
                'class': 'button_new',
                'id': WndName,
                'name': pId, //RepConvTool.GetLabel(pId),
                'style': "float: right; margin: 2px; ",
                //'rel'   : '#' + WndName
            }).button({
                'caption': pId, //RepConvTool.GetLabel(pId)
                'template': 'tpl_button' //(RepConv.settings[RepConv.Cookie+'_imgBtn']) ? 'tpl_grcrt_button' : 'tpl_button'
            });
        return _btn;
    }

    dio.initArray = []
    dio.wndArray = []

    /*******************************************************************************************************************************
     * Radar
     *******************************************************************************************************************************/

    var nb_Radar = 0, DIO_Radar = [];
    var Radar = {
        activate: () => {
            $('<style id="dio_Radar_style"> ' +
                '.dio_rr_town, .dio_rr_player { float: left; width: 240px; max-width: 240px; }' +
                '.dio_rr_points { float: left; width: 40px; text-align: right; }' +
                '.dio_rr_cs_time { float: left; /*width:*/ 105px; text-align: right; margin-right: 5px; }' +
                '.dio_rr_town img, .dio_rr_player img { float: left; }' +
                '#dio_rr_unit { position: relative; display: block; float: left; text-align: right; border: 1px solid #724B08; }' +
                '.option.unit_icon40x40 { float: left; position: relative; border: 1px solid #724B08; margin: 1px; }' +
                '.option.unit_icon40x40.selected { border: 2px solid red; margin: 0px; }' +
                '.dio_bonuses { background: url(' + Home_url + '/img/dio/logo/uX7_.S9_.I7_.S7__20_0.png) 0px 0px;width: 20px; height: 20px; float: right; margin: 0 2px 2px 0;border: 1px solid #8c7878;cursor: pointer; }' +
                '.dio_meteorology { background-position: 0 0; }' +
                '.dio_lighthouse { background-position: -20px 0; }' +
                '.dio_cartography {background-position: -40px 0; }' +
                '.dio_set_sail { background-position: -60px 0; }' +
                '#dio_town_lists_list .option.disabled { color: gray !important; }' +
                '.dio_pagination { padding: 5px;height: 20px; }' +
                '#dio_cs_time>.body>input { text-align:center !important; left: 5px; }' +
                '.dio.radar { background-position: -77px -80px; cursor: pointer;' +
                '#loadingIcon { display: none; z-index: 6; background: url(' + Home_url + '/img/dio/logo/loadingIcon.gif) no-repeat;width: 200px; height: 200px; position: absolute; left: 370px; top: 200px; filter: opacity(0.5);}' +
                '#grepodata { bottom: 17px; position: absolute; right: 10px; }' +
                '#dio.radar .modifiers_container { max-width: 350px; margin-top: 0px; margin-left: 0px; }' +
                '#dio.radar .find { float: left; padding: 3px 5px; margin: 2px; }' +
                '</style>').appendTo('head');

            Radar.DIO_Radar();
        },
        deactivate: () => {
            if (dio.menu[1]) delete dio.menu[1]; // Supprimer la valeur avec la clé 1
            filldiomenu()
            $("dio_Radar_style").remove();
            DIO_Radar.windowclose()
        },
        info: (action) => {
            try {
                let id, name, action_id = action, each_player = $('#player_info.bold h3');
                if (action == "info") each_player = $('#towninfo_towninfo');
                if (action == "alliance") each_player = $('#player_info h3.bold');
                action_id = action_id + nb_Radar


                $(each_player).each(function () {
                    if (!$(this).parent().parent().parent().parent().find('.dio.radar').get(0)) {
                        nb_Radar++

                        if (action == "alliance") {
                            name = $(this).parent().parent().parent().parent().find('.ui-dialog-title').text().trim();
                            $.each(uw.DIO_TOOLS.cacheAlliances, function (allianceId, allianceData) { if (allianceData.name === name.replace(/\ /g, '+')) id = allianceData.id; });
                            if (!id) return;
                            $(this).parent().parent().parent().find('#alliance_points').after('<div id="dio_Radar' + action_id + '" style="width: 23px; height: 23px; float: left;" class="dio radar"></div>')
                            $('#dio_Radar' + action_id).click(function () { DIO_Radar.windowOpen({ alliance: { 'id': id, 'name': name } }) }).tooltip(dio_icon + getTexts("Radar", "Radar"))
                        }
                        else if (action == "player") {
                            name = $(this).parent().parent().find("#player_info h3").text().trim();
                            if (uw.DIO_TOOLS.cachePlayers[name.replace(/ /g, '+')]) id = uw.DIO_TOOLS.cachePlayers[name.replace(/ /g, '+')].id;
                            else return;
                            $(this).parent().parent().find('#player_info h3').before('<div id="dio_Radar' + action_id + '" style="width: 23px; height: 23px; float: left; margin-top: 6px;" class="dio radar"></div>')
                            $('#dio_Radar' + action_id).click(function () { DIO_Radar.windowOpen({ player: { 'id': id, 'name': name } }) }).tooltip(dio_icon + getTexts("Radar", "Radar"))
                        }
                        else if (action == "info") {
                            let _attr = $(this).find($('.info_jump_to_town')).attr('onclick'), _rgx = /\w+:\d+/g, _match, _town = {};
                            _town.name = $(this).find('.game_header.bold').text().trim()
                            while (_match = _rgx.exec(_attr)) { _town[_match[0].split(":")[0]] = _match[0].split(":")[1] }
                            $(this).find('.game_header.bold').append('<div id="dio_Radar' + action_id + '" class="dio radar" style="width: 23px; height: 23px; float: right; margin-top: -1px;"></div>')
                            $('#dio_Radar' + action_id).click(function () { DIO_Radar.windowOpen({ town: { 'id': _town.id, 'name': _town.name, 'ix': _town.x, 'iy': _town.y } }) }).tooltip(dio_icon + getTexts("Radar", "Radar"))
                        }
                    }
                });
            } catch (error) { errorHandling(error, "Radar.info"); }
        },
        DIO_Radar: () => {
            "use strict";

            uw.GameEvents.dio = uw.GameEvents.dio || {};
            uw.GameEvents.dio.radar = {
                find_btn: "dio:radar:find_btn",
                display_towns: "dio:radar:display_towns"
            };
            var _IdS = 'dio_radar';
            var
                _tList,
                _Tlist,
                _Tdist,
                curTown,
                curTownX,
                curTownY,
                curChunk,
                __player = null,
                __ally = null,
                __town = null,
                default_timeCS = DATA.radar.default_timeCS,
                default_points = parseInt(DATA.radar.default_points),
                rGhostAll,
                chunk = {},
                margin = null, /*Math.ceil((GameData.units.colonize_ship2.speed*12)/WMap.getChunkSize()),*/
                checker = (uw.require("map/helpers") || uw.WMap).getTownType,
                resData = {},
                _unitSpeed,
                btn_find = dio.AddBtn(getTexts("Radar", "find"), 'RADAR.BTNFIND'),
                tabAlliances,
                _Thtml,
                _ThtmlPage;
            var sp_cs_lifetime, sp_town_points, sp_player_idle, dd_units, dd_town_lists;
            var cbx_meteorology, cbx_cartography, cbx_set_sail, cbx_unit_movement_boost, cbx_lighthouse, hero_picker, hero_bonus = 0;
            var _adds = null;
            var _pagination;
            var _dioData = [];
            var __allyColors = {};

            function genCheckBox(pName, pChecked) {
                return $('<div/>', { 'class': 'checkbox_new' })
                    .checkbox({
                        caption: '',
                        checked: pChecked,
                        cid: pName
                    }).on("cbx:check", function () {
                        setUnitSpeed()
                    });
            }
            function getHeroesObjForHeroPicker() {
                var a = uw.DM.getl10n("place", "simulator"),
                    b = [{
                        info: a.unassign,
                        value: ""
                    }],
                    runtimes = [];
                $.each(uw.require("enums/runtime_info"), function (key, value) { runtimes.push(value) });
                if (uw.GameData.heroes) {
                    $.each(uw.GameData.heroes, function (a, c) {
                        var d = {
                            value: a,
                            level: c.name,
                            hero_level: 1
                        };
                        ($.inArray(a, runtimes, 0) > -1 && b.push(d))
                    });
                }
                return b;
            }
            function getMargin() {
                if (margin == null) margin = Math.ceil((uw.GameData.units.colonize_ship.speed * 12) / uw.WMap.getChunkSize())
                return margin;
            }
            function getAdds() {
                if (_adds == null) _adds = "meteorology lighthouse cartography unit_movement_boost" + (uw.GameData.buildings.academy.max_level == 30 ? "" : " set_sail");
                return _adds;
            }
            DIO_Radar.getSpCs = function () { return sp_cs_lifetime; }
            DIO_Radar.getThtmlPage = function () { return _ThtmlPage; }
            DIO_Radar.getThtml = function () { return _Thtml; }
            DIO_Radar.setPlayer = function (player_id, player_name) { setPlayer(player_id, player_name); }
            DIO_Radar.setAlly = function (alliance_id, alliance_name) { setAllliance(alliance_id, alliance_name); }
            DIO_Radar.setGhost = function () { setGhost() }
            DIO_Radar.setCurrentTown = function () { setCurrentTown(); }
            DIO_Radar.getFirstTown = function () {
                genTownList();
                generateTime();
                return _Tlist[_Tdist[0]] || null;
            }
            function activeDeactiveShowCities() {
                if (__town != null) {
                    dd_town_lists.setExclusions([''])
                } else if (rGhostAll && rGhostAll.getValue() == 'RGHOST' || __player != null || __ally != null) {
                    dd_town_lists.setValue('all');
                    dd_town_lists.setExclusions(['player', 'alliance', 'allypacts', 'pacts', 'enemies'])
                } else {
                    dd_town_lists.setExclusions([''])
                }
            }
            function setPlayer(player_id, player_name) {
                __player = { 'id': player_id, 'name': player_name };
                __ally = null;
                __town = null;
            }
            function setAllliance(alliance_id, alliance_name) {
                __player = null;
                __ally = { 'id': alliance_id, 'name': alliance_name };
                __town = null;
            }
            function setTown(town_id, town_name, town_ix, town_iy) {
                __player = null;
                __ally = null;
                __town = { 'id': town_id, 'name': town_name, 'ix': town_ix, 'iy': town_iy };
            }
            function setGhost() {
                __player = null;
                __ally = null;
                __town = null;
            }
            function getUnitSpeed4Town(townId) {
                // var _speed = 0
                if (url_dev) console.group("getUnitSpeed4Town")
                if (url_dev) console.log(townId)
                var bonus = 0, boost = 0;
                bonus += (uw.GameData.units[dd_units.getValue()].is_naval && uw.MM.getModels().Town[townId].getResearches().get('cartography')) ? uw.GameData.research_bonus.cartography_speed : 0
                bonus += (uw.GameData.buildings.academy.max_level > 30 && dd_units.getValue() == "colonize_ship" && uw.MM.getModels().Town[townId].getResearches().get('set_sail')) ? uw.GameData.research_bonus.colony_ship_speed : 0
                bonus += (uw.GameData.units[dd_units.getValue()].is_naval && uw.MM.getModels().Town[townId].getBuildings().get('lighthouse') == 1) ? uw.GameData.additional_runtime_modifier.lighthouse_speed_bonus : 0
                bonus += (!uw.GameData.units[dd_units.getValue()].is_naval && uw.MM.getModels().Town[townId].getResearches().get('meteorology')) ? uw.GameData.research_bonus.meteorology_speed : 0
                boost += (cbx_unit_movement_boost.isChecked() && !$('.dio_modifiers .modifier_icon.unit_movement_boost').hasClass('inactive')) ? 0.3 : 0
                if (url_dev) console.log("bonus=" + bonus)
                if (url_dev) console.log("boost=" + boost)
                if (url_dev) console.log('result = ' + uw.GameData.units[dd_units.getValue()].speed * (1 + bonus)) * (1 + hero_bonus + boost)
                if (url_dev) console.groupEnd()
                return (uw.GameData.units[dd_units.getValue()].speed * (1 + bonus)) * (1 + hero_bonus + boost)
                // *(1+(cbx_unit_movement_boost.isChecked() && !$('.dio_modifiers .modifier_icon.unit_movement_boost').hasClass('inactive'))?0.3:0)
            }
            function getUnitSpeed() {
                var bonus = 0, boost = 0;
                if (url_dev) console.group("getUnitSpeed")
                bonus += (uw.GameData.units[dd_units.getValue()].is_naval && cbx_cartography.isChecked() && !$('.dio_modifiers .modifier_icon.cartography').hasClass('inactive')) ? uw.GameData.research_bonus.cartography_speed : 0
                bonus += (uw.GameData.buildings.academy.max_level > 30 && dd_units.getValue() == "colonize_ship" && cbx_set_sail.isChecked() && !$('.dio_modifiers .modifier_icon.set_sail').hasClass('inactive')) ? uw.GameData.research_bonus.colony_ship_speed : 0
                bonus += (uw.GameData.units[dd_units.getValue()].is_naval && cbx_lighthouse.isChecked() && !$('.dio_modifiers .modifier_icon.lighthouse').hasClass('inactive')) ? uw.GameData.additional_runtime_modifier.lighthouse_speed_bonus : 0
                bonus += (!uw.GameData.units[dd_units.getValue()].is_naval && cbx_meteorology.isChecked() && !$('.dio_modifiers .modifier_icon.meteorology').hasClass('inactive')) ? uw.GameData.research_bonus.meteorology_speed : 0
                boost += (cbx_unit_movement_boost.isChecked() && !$('.dio_modifiers .modifier_icon.unit_movement_boost').hasClass('inactive')) ? 0.3 : 0
                if (url_dev) console.log("bonus=" + bonus)
                if (url_dev) console.log("boost=" + boost)
                if (url_dev) console.log('result = ' + uw.GameData.units[dd_units.getValue()].speed * (1 + bonus)) * (1 + hero_bonus + boost)
                if (url_dev) console.groupEnd()
                return (uw.GameData.units[dd_units.getValue()].speed * (1 + bonus)) * (1 + hero_bonus + boost)
                // return (GameData.units[dd_units.getValue()].speed*(1+bonus))
                // *(1+(cbx_unit_movement_boost.isChecked() && !$('.dio_modifiers .modifier_icon.unit_movement_boost').hasClass('inactive'))?0.3:0)
            }
            function setUnitSpeed() {
                if (url_dev) console.group("setUnitSpeed")
                if (__town != null) {
                    // curTown = MM.getModels().Town[Game.townId],
                    curTownX = __town.ix;
                    curTownY = __town.iy;
                    curChunk = uw.WMap.toChunk(curTownX, curTownY).chunk;
                    resData[__town.id] = {};//resData[__town.id]||{},
                    _unitSpeed = getUnitSpeed()//GameData.units[dd_units.getValue()].speed
                    if (url_dev) console.log("__town " + _unitSpeed)
                } else {
                    // var bonus = 0;
                    curTown = uw.MM.getModels().Town[uw.Game.townId];
                    curTownX = curTown.get('island_x');
                    curTownY = curTown.get('island_y');
                    curChunk = uw.WMap.toChunk(curTownX, curTownY).chunk;
                    resData[uw.Game.townId] = {};//resData[Game.townId]||{},
                    _unitSpeed = getUnitSpeed4Town(uw.Game.townId) //GameData.units[dd_units.getValue()].speed*(1+bonus)
                    if (url_dev) console.log("! __town " + _unitSpeed)
                }
                if (url_dev) console.groupEnd()
                $('.dio_modifiers .modifier_icon').removeClass('inactive')
                cbx_meteorology.enable()
                cbx_cartography.enable()
                cbx_set_sail.enable()
                cbx_lighthouse.enable()
                if (uw.GameData.units[dd_units.getValue()].is_naval) {
                    $('.dio_modifiers .modifier_icon.meteorology').addClass('inactive')
                    cbx_meteorology.disable()
                } else {
                    $('.dio_modifiers .modifier_icon.cartography').addClass('inactive')
                    $('.dio_modifiers .modifier_icon.set_sail').addClass('inactive')
                    $('.dio_modifiers .modifier_icon.lighthouse').addClass('inactive')
                    cbx_cartography.disable()
                    cbx_set_sail.disable()
                    cbx_lighthouse.disable()
                }

                var pk = uw.GameData.units.colonize_ship.speed;
                var maxH = Math.max(4, Math.floor(-1.875 * 1 / pk * uw.GameData.units[dd_units.getValue()].speed + 25.875)) * 60 * 60
                // console.log(maxH);
                sp_cs_lifetime.setMax(uw.DateHelper.readableSeconds(maxH))
                if (sp_cs_lifetime.getTimeValueAsSeconds() > maxH) {
                    sp_cs_lifetime.setValue(uw.DateHelper.readableSeconds(maxH))
                }
            }
            function ddCitiesList() {
                tabAlliances = {
                    'all': { name: uw.DM.getl10n('report').inbox.filter_types.all, value: [] },
                    'player': { name: uw.DM.getl10n('custom_colors').your_cities, value: [uw.Game.player_id] },
                    'alliance': { name: uw.DM.getl10n('custom_colors').your_alliance, value: [uw.MM.checkAndPublishRawModel('Player', { id: uw.Game.player_id }).getAllianceId()] },
                    'allypacts': { name: uw.DM.getl10n('custom_colors').your_alliance + " + " + uw.DM.getl10n('custom_colors').pacts, value: [uw.MM.checkAndPublishRawModel('Player', { id: uw.Game.player_id }).getAllianceId()] },
                    'pacts': { name: uw.DM.getl10n('custom_colors').pacts, value: [] },
                    'enemies': { name: uw.DM.getl10n('custom_colors').enemies, value: [] },

                }
                if (uw.MM.checkAndPublishRawModel('Player', { id: uw.Game.player_id }).getAllianceId() != null) {
                    tabAlliances.alliance = { name: uw.DM.getl10n('custom_colors').your_alliance, value: [uw.MM.checkAndPublishRawModel('Player', { id: uw.Game.player_id }).getAllianceId()] }
                    var what;
                    $.each(uw.MM.getOnlyCollectionByName("AlliancePact").models, function (ii, ee) {
                        if (!ee.getInvitationPending()) {
                            switch (ee.getRelation()) {
                                case "war":
                                    what = "enemies";
                                    break;
                                case "peace":
                                    what = "pacts";
                                    break;
                            }
                            if (what == "pacts") tabAlliances.allypacts.value.push(((ee.getAlliance1Id() == uw.Game.alliance_id) ? ee.getAlliance2Id() : ee.getAlliance1Id()))
                            tabAlliances[what].value.push(((ee.getAlliance1Id() == uw.Game.alliance_id) ? ee.getAlliance2Id() : ee.getAlliance1Id()))
                        }
                    })
                }
                var _result = [];
                $.each(tabAlliances, function (ind, elem) {
                    _result.push({ 'name': elem.name, 'value': ind });
                })
                return _result;
            }
            function setCurrentTown() {
                _tList = [];
                _Tlist = {};
                _Tdist = [];
                setUnitSpeed();
            }
            function hex2rgba(hex, opacity) {
                hex = hex.replace('#', '');
                var
                    r = parseInt(hex.substring(0, 2), 16),
                    g = parseInt(hex.substring(2, 4), 16),
                    b = parseInt(hex.substring(4, 6), 16),
                    result = 'rgba(' + r + ',' + g + ',' + b + ',' + opacity / 100 + ')';
                return result;
            }
            function getServerData() {//checkReload(){
                $.ajax({
                    type: "GET",
                    /*//url: 'https://www.grcrt.net/json_rpc.php',
                    data : {
                        'method' : 'getTown4Radar',
                        'world' : uw.Game.world_id,
                        'town_id' : (__town) ? __town.id : uw.Game.townId,
                        'margin' : sp_cs_lifetime.getTimeValueAsSeconds()*_unitSpeed/50
                    },*/
                    url: 'https://api.grepodata.com/town/radar',
                    data: {
                        //'method' : 'getTown4Radar',
                        'world': uw.Game.world_id,
                        'town_id': (__town) ? __town.id : uw.Game.townId,
                        'margin': sp_cs_lifetime.getTimeValueAsSeconds() * _unitSpeed / 50
                    },

                    dataType: "json",
                    async: false,
                    cache: true
                })
                    .done(function (data) {
                        _dioData = data
                    })
            }
            function getData() {
                resData[curTownId()] = {}
                if (Object.size(resData[curTownId()]) == 0) {
                    // $.each(chunk, function(indd,data){
                    $.each(_dioData.towns, function (indt, town) {
                        if (checker(town) == 'town') {
                            resData[curTownId()][town.id] = town;
                        }
                    })
                    // })
                }
                return resData[curTownId()];
            }
            function curTownId() {
                if (__town != null) return __town.id;
                return uw.Game.townId;
            }
            function getTownModel() {
                var townModel, chunks, data;
                if (__town == null) {
                    var
                        __tmp = uw.MM.getModels().Town[uw.Game.townId];
                    chunks = uw.WMap.toChunk(__tmp.get('island_x'), __tmp.get('island_y')).chunk;
                    data = _dioData;//chunk[chunks.x+'_'+chunks.y];
                    $.each(data.towns, function (indt, town) {
                        if (checker(town) == 'town') {
                            if (town.id == __tmp.id) {
                                townModel = generateTown(town);
                            }
                        }
                    })
                } else {
                    chunks = uw.WMap.toChunk(__town.ix, __town.iy).chunk;
                    data = _dioData;//chunk[chunks.x+'_'+chunks.y];
                    if (url_dev) console.group("__town")
                    if (url_dev) console.log(__town)
                    if (url_dev) console.groupEnd()
                    $.each(data.towns, function (indt, town) {
                        if (checker(town) == 'town') {
                            if (town.id == __town.id) {
                                townModel = generateTown(town);
                            }
                        }
                    })
                }
                // console.groupEnd()
                return townModel;
            }
            function generateTown(a) {
                if (checker(a) != 'town') {
                    return null;
                }
                var elTown = {
                    'id': a.id,
                    'ix': a.x,
                    'iy': a.y,
                    'abs_x': a.abs_x,
                    'abs_y': a.abs_y,
                    'name': a.name,
                    'player_id': a.player_id,
                    'player_name': a.player_name,
                    'alliance_id': a.alliance_id,
                    'alliance_name': a.alliance_name,
                    'points': a.points,
                    'reservation': null, //a.reservation
                    'href': "#" +
                        btoa(
                            JSON.stringify({
                                'id': parseInt(a.id),
                                'ix': a.x,
                                'iy': a.y,
                                'tp': ((null !== a.player_id) ? 'town' : 'ghost_town'),
                                'name': a.name
                            })
                                .replace(/[\u007f-\uffff]/g,
                                    function (c) {
                                        return '\\u' + ('0000' + c.charCodeAt(0).toString(16)).slice(-4);
                                    }
                                )
                        ),
                    // 'popup' : (!WMap.createTownPopup)?WMap.createTownTooltip('town',a):WMap.createTownPopup('town',a),
                    'flag_type': a.flag_type,
                    'fc': getPlayerColor(a.player_id, a.alliance_id)
                }
                //         a.id += "", a.id = a.id.replace("=", "");
                //         var d = (require("map/helpers")).map2Pixel(a.x, a.y)
                //         elTown.abs_x = d.x+a.ox,
                //         elTown.abs_y = d.y+a.oy
                return elTown;
            }

            function genTownList() {
                var what;
                __allyColors[uw.Game.alliance_id] = 'OWN_ALLIANCE';
                $.each(uw.MM.getOnlyCollectionByName("AlliancePact").models, function (ii, ee) {
                    if (!ee.getInvitationPending()) {
                        switch (ee.getRelation()) {
                            case "war":
                                what = "ENEMY";
                                break;
                            case "peace":
                                what = "PACT";
                                break;
                        }
                        __allyColors[(ee.getAlliance1Id() == uw.Game.alliance_id) ? ee.getAlliance2Id() : ee.getAlliance1Id()] = what
                    }
                })
                if (__player != null) genPlayer();
                else if (__ally != null) genAlly();
                else if (__town != null) genTown();
                else if (rGhostAll.getValue() != 'RGHOST') genAll();
                else genGhost();
                return true;
            }

            function genPlayer() {
                _tList = []
                $.each(getData(), function (ind, elem) {
                    var res = generateTown(elem);
                    if (res != null && res.player_id == __player.id) {
                        _tList.push(res);
                    }
                })
            }

            function genAlly() {
                _tList = []
                $.each(getData(), function (ind, elem) {
                    var res = generateTown(elem);
                    if (res != null && res.alliance_id == __ally.id) {
                        _tList.push(res);
                    }
                })
            }

            function genTown() {
                _tList = []
                $.each(getData(), function (ind, elem) {
                    var res = generateTown(elem);
                    if (res != null && res.id != __town.id) {
                        _tList.push(res);
                    }
                })
            }

            function genAll() {
                _tList = []
                $.each(getData(), function (ind, elem) {
                    var res = generateTown(elem);
                    if (elem.id != uw.Game.townId && res != null) {
                        _tList.push(res);
                    }
                })
            }

            function genGhost() {
                _tList = []
                $.each(getData(), function (ind, elem) {
                    var res = generateTown(elem);
                    if (res != null && res.player_id == null) {
                        _tList.push(res);
                    }
                })
            }

            DIO_Radar.getTownList = function () { return _Tlist; }

            function generateTime() {
                var
                    _curTown,
                    _offset = 900 / uw.Game.game_speed,
                    idCurTown = curTownId(),
                    elCurTown = getTownModel(), //MM.getModels().Town[idCurTown],
                    elTown = {},
                    _MDTown,
                    ___unitSpeed,
                    __timeInSec;
                _Tlist = {};
                _Tdist = [];
                $.each(_tList, function (indTown, elTown) {
                    var _dist = Math.floor(
                        $.toe.calc.getDistance(
                            { 'x': elCurTown.abs_x, 'y': elCurTown.abs_y },
                            { 'x': elTown.abs_x, 'y': elTown.abs_y }
                        )
                    )
                    if ((elCurTown.ix != elTown.ix || elCurTown.iy != elTown.iy) && !(uw.GameData.units[dd_units.getValue()].flying || uw.GameData.units[dd_units.getValue()].is_naval)) {
                    } else {
                        ___unitSpeed = (uw.MM.getModels().Town[elTown.id]) ? getUnitSpeed4Town(elTown.id) : _unitSpeed;
                        __timeInSec = Math.round(50 * _dist / ___unitSpeed + _offset)
                        if (url_dev) console.log("generateTime ___unitSpeed=" + ___unitSpeed + " vs _unitSpeed=" + _unitSpeed)
                        if (_Tlist[__timeInSec] == undefined) {
                            _Tlist[__timeInSec] = { 'time': 0, 'towns': [] };
                            _Tdist.push(__timeInSec)
                        }
                        _Tlist[__timeInSec].towns.push(elTown);
                        _Tlist[__timeInSec].timeInSec = Math.round(50 * _dist / ___unitSpeed + _offset);
                        _Tlist[__timeInSec].time = uw.DateHelper.readableSeconds(_Tlist[__timeInSec].timeInSec)
                    }
                })
                var swapped;
                do {
                    swapped = false;
                    for (var i = 0; i < _Tdist.length - 1; i++) {
                        if (_Tdist[i] > _Tdist[i + 1]) {
                            var temp = _Tdist[i];
                            _Tdist[i] = _Tdist[i + 1];
                            _Tdist[i + 1] = temp;
                            swapped = true;
                        }
                    }
                } while (swapped);
                return true;
            }

            function displayTownListHeader() {
                var n = uw.DM.getl10n('map');
                function e(a) {
                    if (!a.reservation) return "";
                    if ("added" === a.reservation.state) {
                        if ("ally" === a.reservation.type) return n.can_reserve;
                        else return n.reserved_by_alliance;
                    } else if ("reserved" === a.reservation.state) {
                        var _icon = '<span class="reservation_tool icon small ' + a.reservation.state + ' ' + a.reservation.type + '"></span>';
                        if ("own" === a.reservation.type) return _icon + n.reserved_for_you;
                        else if ("ally" === a.reservation.type) return _icon + n.reserved_for(a.reservation.player_link);
                        else return _icon + n.reserved_for_alliance(a.reservation.player_link, a.reservation.alliance_link);
                    }
                }
                _pagination = $('<div/>', { 'class': "dio_pagination" })
                $('#dio_radar_result')
                    .html("")
                    .append(
                        $('<div/>', { 'class': "game_header bold", 'style': "height:18px;" })
                            .append($('<div/>', { 'class': 'dio_rr_town', 'style': "float:left;" }).html(getTexts("Radar", "townname")))
                            .append($('<div/>', { 'class': 'dio_rr_cs_time', 'style': "float:left; text-align: center; width: 220px" }).html(getTexts("Radar", "unittime")))
                            .append($('<div/>', { 'class': 'dio_rr_player', 'style': "float:left;" }).html(getTexts("Radar", "townowner")))
                            .append($('<div/>', { 'class': 'dio_rr_player', 'style': "float:left;" }).html(getTexts("Radar", "townreserved"))))
                    .append(
                        $('<div/>', { 'style': 'min-height: 350px; max-height: 350px; overflow-y: hidden; overflow-x: hidden; border: 1px solid grey; position: relative;', 'class': 'js-scrollbar-viewport' })
                            .append($('<ul/>', { 'class': 'game_list js-scrollbar-content', 'style': 'width: 100%;' })))
                    .append(_pagination)

                var _qq = 0, __owner, _show = true, __addons;
                _ThtmlPage = 0; _Thtml = {}
                $.each(_Tdist, function (ind, _key) {
                    if (sp_cs_lifetime.getTimeValueAsSeconds() >= _Tlist[_key].timeInSec) {
                        $.each(_Tlist[_key].towns, function (iiT, eeT) {
                            if (sp_town_points.getValue() <= eeT.points && (parseFloat(uw.DIO_TOOLS.player_idle[eeT.player_id]) >= sp_player_idle.getValue() && ((__player != null) || (__ally != null) || (__town != null) || (rGhostAll.getValue() != 'RGHOST')) || (rGhostAll && rGhostAll.getValue() == 'RGHOST'))) {
                                switch (dd_town_lists.getValue()) {
                                    case 'player':
                                        _show = eeT.player_id == uw.Game.player_id
                                        break;
                                    case 'alliance':
                                        _show = tabAlliances[dd_town_lists.getValue()].value.contains(eeT.alliance_id || 0);
                                        break;
                                    case 'allypacts':
                                        _show = tabAlliances[dd_town_lists.getValue()].value.contains(eeT.alliance_id || 0);
                                        break;
                                    case 'pacts':
                                        _show = tabAlliances[dd_town_lists.getValue()].value.contains(eeT.alliance_id || 0);
                                        break;
                                    case 'enemies':
                                        _show = tabAlliances[dd_town_lists.getValue()].value.contains(eeT.alliance_id || 0);
                                        break;
                                    default:
                                        _show = true;
                                }

                                if (_show) {
                                    if (_qq % 20 == 0) {
                                        // _ThtmlPage++;
                                        _Thtml[(_qq / 20).toString()] = [];
                                    }
                                    eeT.timeInSec = _Tlist[_key].timeInSec
                                    eeT.time = _Tlist[_key].time
                                    //                            eeT.fc = getPlayerColor(eeT.player_id, eeT.alliance_id)//(eeT.href,__allyColors)
                                    _Thtml[Math.floor(_qq++ / 20).toString()].push(eeT);
                                }
                            }
                        })
                    }
                })
                $.Observer(uw.GameEvents.dio.radar.display_towns).publish()
            }


            function pagination() {
                var _pmin = 1, _pmax = Object.size(_Thtml), _btn = true;
                _pagination
                    .html("")
                $.each(_Thtml, function (ii, elem) {

                    if (parseInt(ii) + 1 == _pmin || parseInt(ii) + 1 == _pmax || parseInt(ii) == _ThtmlPage - 1 || parseInt(ii) == _ThtmlPage || parseInt(ii) == _ThtmlPage + 1) {
                        _btn = true
                        if (_ThtmlPage == (parseInt(ii))) {
                            _pagination.append($('<strong/>', { 'class': 'paginator_bg', 'id': 'paginator_selected' }).html(parseInt(ii) + 1))

                        } else {
                            _pagination.append(
                                $('<a/>', { 'class': 'paginator_bg', 'href': '#n' }).html(parseInt(ii) + 1).click(function () {
                                    _ThtmlPage = parseInt($(this).html()) - 1;
                                    $.Observer(uw.GameEvents.dio.radar.display_towns).publish()
                                })
                            )
                        }
                    } else if (_btn) {
                        _btn = false
                        _pagination.append($('<strong/>', { 'class': 'paginator_bg', 'id': 'paginator_inactive' }).html("..."))
                    }
                })
            }

            function displayTownList() {
                if (_ThtmlPage >= Object.size(_Thtml)) return;
                var n = uw.DM.getl10n('map');
                var _qq = 0, __owner, __addons;
                function e(a) {
                    if (!a.reservation) return "";
                    if ("added" === a.reservation.state) {
                        if ("ally" === a.reservation.type) return n.can_reserve;
                        else return n.reserved_by_alliance;
                    } else if ("reserved" === a.reservation.state) {
                        var _icon = '<span class="reservation_tool icon small ' + a.reservation.state + ' ' + a.reservation.type + '"></span>';
                        if ("own" === a.reservation.type) return _icon + n.reserved_for_you;
                        else if ("ally" === a.reservation.type) return _icon + n.reserved_for(a.reservation.player_link);
                        else return _icon + n.reserved_for_alliance(a.reservation.player_link, a.reservation.alliance_link);
                    }
                }
                // _ThtmlPage = 0, _Thtml={}
                $('#dio_radar_result ul').html("");
                $.each(_Thtml[_ThtmlPage.toString()], function (ind, eeT) {
                    __owner = (eeT.player_id == null) ? '<div style="margin-top: 6px;"> ' + uw.DM.getl10n('common', 'ghost_town') + '</div>' : '<img src="' + uw.Game.img() + '/game/icons/player.png" />' + uw.hCommon.player(eeT.player_name, eeT.player_id)
                    __owner += (eeT.alliance_name == null) ? '' : '<br/>' + '<img src="' + uw.Game.img() + '/game/icons/ally.png" />' + uw.hCommon.alliance('n', eeT.alliance_name, eeT.alliance_id)
                    __addons = ''
                    if (uw.MM.getModels().Town[eeT.id]) {
                        __addons += (uw.GameData.units[dd_units.getValue()].is_naval && uw.MM.getModels().Town[eeT.id].getResearches().get('cartography')) ? '<div class="dio_bonuses dio_cartography"></div>' : '';
                        __addons += (uw.dd_units.getValue() == "colonize_ship" && uw.MM.getModels().Town[eeT.id].getResearches().get('set_sail')) ? '<div class="dio_bonuses dio_set_sail"></div>' : '';
                        __addons += (uw.GameData.units[dd_units.getValue()].is_naval && uw.MM.getModels().Town[eeT.id].getBuildings().get('lighthouse') == 1) ? '<div class="dio_bonuses dio_lighthouse"></div>' : '';
                        __addons += !(uw.GameData.units[dd_units.getValue()].is_naval && uw.MM.getModels().Town[eeT.id].getResearches().get('meteorology')) ? '<div class="dio_bonuses dio_meteorology"></div>' : '';
                    }
                    $('#dio_radar_result ul').append(
                        $('<li/>', { 'class': ((++_qq % 2) ? 'even' : 'odd') })
                            .append($('<div/>', { 'class': "dio_rr_town" })
                                .append($('<a/>', { 'class': "gp_town_link", 'href': eeT.href }).html(eeT.name))
                                .append($('<br/>'))
                                .append($('<span/>', { 'class': '' }).html('<img src="' + uw.Game.img() + '/game/icons/points.png" /> ' + n.points(eeT.points)))
                                .append(__addons)
                                .css('border-left', '5px solid #' + (eeT.fc || "f00"))
                                .css('background-color', hex2rgba(eeT.fc || "f00", 10)))
                            .append($('<div/>', { 'class': 'dio_rr_cs_time' }).append($('<span/>', { 'class': 'way_duration' }).html('~' + eeT.time)))
                            .append($('<div/>', { 'class': 'dio_rr_cs_time' }).append($('<span/>', { 'class': 'arrival_time', 'data-sec': eeT.timeInSec })))
                            .append($('<div/>', { 'class': 'player_name dio_rr_player' }).html(__owner))
                            .append($('<div/>', { 'class': 'player_name dio_rr_player' }).html(e(eeT)))
                            .append($('<br/>', { 'style': 'clear:both' }))
                    )
                })
                $.each(getAdds().split(" "), function (i, o) {
                    $('#dio_radar_result ul .dio_' + o + ':not(.dio_done)').tooltip(dio.getTooltip(o)).addClass('dio_done')
                })
                $.each($(".dio_rr_cs_time .arrival_time:not(.dio_done)"), function (i, elem) {
                    $(elem).text($(elem).data('sec') + "").updateTime().addClass('dio_done')
                })
                // _scrollBar();
                pagination();
            }

            function whatFinder() {
                if (__player != null) {
                    return '<img src="' + uw.Game.img() + '/game/icons/player.png" />' +
                        uw.hCommon.player(
                            // btoa(
                            //     JSON.stringify({"name":__player.name,"id":__player.id})
                            //         .replace(/[\u007f-\uffff]/g,
                            //             function(c) {
                            //               return '\\u'+('0000'+c.charCodeAt(0).toString(16)).slice(-4);
                            //             }
                            //         )
                            // ),
                            __player.name,
                            __player.id
                        );
                } else if (__ally != null) {
                    return '<img src="' + uw.Game.img() + '/game/icons/ally.png" />' +
                        uw.hCommon.alliance('n', __ally.name, __ally.id);
                } else if (__town != null) {
                    return '<div style="float:right">' +
                        '<img src="' + uw.Game.img() + '/game/icons/town.png" style="float:left"/>' +
                        '<a class="gp_town_link" href="' + btoa(JSON.stringify({
                            'id': __town.id,
                            'ix': __town.ix,
                            'iy': __town.iy,
                            'tp': 'town',
                            'name': __town.name
                        })) + '">' + __town.name + '</a>' +
                        '</div>';
                } else {
                    rGhostAll = $('<div/>', {
                        'class': 'radiobutton',
                        'id': 'dio_rghost'
                    })
                        .radiobutton({
                            value: 'RGHOST',
                            template: "tpl_radiobutton",
                            options: [{
                                value: 'RGHOST',
                                name: uw.DM.getl10n('common', 'ghost_town')
                            }, {
                                value: 'RALL',
                                name: getTexts("Radar", "all")
                            }]
                        })
                        .on("rb:change:value", function (a, d, e) {
                            activeDeactiveShowCities()
                        })
                    return rGhostAll;
                    //return DM.getl10n('common','ghost_town');
                }
            }

            function getPlayerColor(player_id, alliance_id) {
                var
                    _mmcc = uw.MM.getOnlyCollectionByName("CustomColor"),
                    _defc = uw.require("helpers/default_colors"),
                    _ffty = uw.require("enums/filters"),
                    // _json = JSON.parse(RepConvTool.Atob(hash)),
                    _color = undefined;
                if (player_id == uw.Game.player_id) {
                    _color = _defc.getDefaultColorForPlayer(uw.Game.player_id)
                }
                if (!_color && !player_id && !alliance_id) {
                    _color = '666666';
                }

                if (!_color) {
                    _color = _mmcc.getCustomColorByIdAndType(_ffty.FILTER_TYPES.PLAYER, player_id) && _mmcc.getCustomColorByIdAndType(_ffty.FILTER_TYPES.PLAYER, player_id).getColor()
                }

                if (!_color) {
                    if (player_id && alliance_id) {
                        if (alliance_id == uw.Game.alliance_id) {
                            _color = (
                                _mmcc.getCustomColorByIdAndType(_ffty.ALLIANCE_TYPES.OWN_ALLIANCE, alliance_id) &&
                                _mmcc.getCustomColorByIdAndType(_ffty.ALLIANCE_TYPES.OWN_ALLIANCE, alliance_id).getColor()
                                ||
                                _defc.getDefaultColorForAlliance(alliance_id)
                            )
                        } else {
                            _color = (
                                (
                                    __allyColors[alliance_id] &&
                                    (
                                        _mmcc.getCustomColorByIdAndType(_ffty.FILTER_TYPES[__allyColors[alliance_id]], alliance_id) &&
                                        _mmcc.getCustomColorByIdAndType(_ffty.FILTER_TYPES[__allyColors[alliance_id]], alliance_id).getColor()
                                        ||
                                        _defc.getDefaultColorForAlliance(alliance_id)
                                    )
                                )
                                ||
                                (
                                    alliance_id &&
                                    (
                                        _mmcc.getCustomColorByIdAndType(_ffty.FILTER_TYPES.ALLIANCE, alliance_id) &&
                                        _mmcc.getCustomColorByIdAndType(_ffty.FILTER_TYPES.ALLIANCE, alliance_id).getColor()
                                        ||
                                        _defc.getDefaultColorForAlliance(alliance_id)
                                    )
                                )
                            )
                        }
                    } else {
                        _color = _defc.getDefaultColorForPlayer(player_id, uw.Game.player_id)
                    }
                }
                return _color;
            }

            function header() {
                cbx_meteorology = genCheckBox('dio_rr_meteorology', (__town == null && uw.MM.getModels().Town[uw.Game.townId].getResearches().get('meteorology'))),
                    cbx_cartography = genCheckBox('dio_rr_cartography', (__town == null && uw.MM.getModels().Town[uw.Game.townId].getResearches().get('cartography'))),
                    cbx_set_sail = genCheckBox('dio_rr_set_sail', (__town == null && uw.MM.getModels().Town[uw.Game.townId].getResearches().get('set_sail'))),
                    cbx_unit_movement_boost = genCheckBox('dio_rr_unit_movement_boost', false),
                    cbx_lighthouse = genCheckBox('dio_rr_lighthouse', (__town == null && uw.MM.getModels().Town[uw.Game.townId].getBuildings().get('lighthouse') == 1));
                hero_picker = (uw.GameDataHeroes.areHeroesEnabled())
                    ? $('<div/>', { 'class': 'modifier hero_modifier', 'style': 'margin-right: 0px; margin-top: 1px;' })
                        .heroPicker({
                            options: getHeroesObjForHeroPicker(),
                            should_have_remove_and_change_btn: !1,
                            should_have_level_btn: !0,
                            confirmation_window: null
                        })
                        .on("hd:change:value", function (a, b, c) {
                            hero_bonus = (b != "") ? uw.GameData.heroes[b].description_args[1].value : 0;
                            setUnitSpeed()
                        })
                        .on("sp:change:value", function (a, b, c) {
                            hero_bonus = uw.GameData.heroes[hero_picker.getValue()].description_args[1].value + uw.GameData.heroes[hero_picker.getValue()].description_args[1].level_mod * b;
                            setUnitSpeed()
                        }).css({ 'width': '75px', 'text-align': 'left' })
                    : null;

                return $('<div/>', { 'id': 'dio_radar' })
                    .append(
                        $('<div/>', { 'style': 'float: left; padding: 3px 5px; margin: 2px;' })
                            .append(
                                $('<span/>').html(getTexts("Radar", "find") + ': ')
                            )
                            .append(
                                whatFinder()
                            )
                    )
                    .append(
                        $('<div/>', { 'style': 'float:right; margin: 5px 10px 0 0' })
                            .append(
                                (dio.AddBtn(dio_icon + getTexts("Radar", "btnsavedefault"), 'RADAR.BTNSAVEDEFAULT'))
                                    .click(function () {
                                        try {
                                            default_timeCS = sp_cs_lifetime.getValue();
                                            default_points = sp_town_points.getValue();
                                            DATA.radar.default_timeCS = default_timeCS;
                                            DATA.radar.default_points = default_points;
                                            saveValue(WID + "_radar", JSON.stringify(DATA.radar));
                                            setTimeout(function () {
                                                HumanMessage.success('MSGHUMAN.OK'); //RepConvTool.GetLabel('MSGHUMAN.OK')
                                            }, 0);
                                        } catch (err) {
                                            //                                            if (url_dev) console.log(RepConvTool.getCaller(arguments.callee.toString()));
                                            setTimeout(function () {
                                                HumanMessage.error('MSGHUMAN.ERROR'); //RepConvTool.GetLabel('MSGHUMAN.ERROR')
                                            }, 0)
                                        }
                                    })
                            )
                            .append(
                                (btn_find)
                                    .click(function () {
                                        $.Observer(uw.GameEvents.dio.radar.find_btn).publish()
                                    })
                            )
                    )
                    .append($('<br/>', { 'style': 'clear:both' }))
                    .append($('<div/>', { 'id': 'dio_rr_unit', 'class': 'unit_icon50x50 colonize_ship', 'style': 'margin:2px 5px 0 5px; cursor: pointer;' }))
                    .append($('<div/>', { 'style': 'float:left' })
                        .append($('<div/>', { 'style': 'padding: 3px 5px; margin: 2px;' }).html(getTexts("Radar", "maxunittime")))
                        .append($('<div/>', { 'id': 'dio_cs_time', 'class': 'spinner', 'style': 'width: 100px; float: right; margin: 2px;' }))
                    )
                    .append($('<div/>', { 'style': 'float:left' })
                        .append($('<div/>', { 'style': 'padding: 3px 5px; margin: 2px;' }).html(getTexts("Radar", "townpoints")))
                        .append($('<div/>', { 'id': 'dio_town_points', 'class': 'spinner_horizontal', 'style': 'width: 100px; float: right; margin: 2px;' })))
                    .append($('<div/>', { 'style': 'float:left' })
                        .append($('<div/>', { 'style': 'padding: 3px 5px; margin: 2px;' }).html(getTexts("Stats", "inactive")))
                        .append($('<div/>', { 'id': 'dio_player_idle', 'class': 'spinner_horizontal', 'style': 'width: 80px; float: right; margin: 2px;' }))
                    )
                    .append($('<div/>', { 'style': 'float:left' })
                        .append($('<div/>', { 'style': 'padding: 3px 5px; margin: 2px;' }).html(getTexts("Radar", "showcities")))
                        .append($('<div/>', { 'id': 'dio_town_lists', 'class': 'dropdown default', 'style': 'width: 155px; float: right; margin: 2px 2px 0px 2px;' }))
                    )
                    .append($('<div/>', { 'class': "runtime_info dio_modifiers", 'style': "float: left;" })
                        .append($('<div/>', { 'class': "modifiers_container", 'style': "max-width: 350px;margin-top: 0px;margin-left: 0px;" })
                            .append($('<div/>', { 'class': "other_modifiers" })
                                .append(hero_picker)
                                .append($('<div/>', { 'class': "modifier", 'style': "margin-right: 5px;" }).append($('<div/>', { 'class': "modifier_icon research_icon research40x40 meteorology" })).append(cbx_meteorology))
                                .append($('<div/>', { 'class': "modifier", 'style': "margin-right: 5px;" }).append($('<div/>', { 'class': "modifier_icon research_icon research40x40 cartography" })).append(cbx_cartography))
                                .append($('<div/>', { 'class': "modifier", 'style': "margin-right: 5px;" + (uw.GameData.buildings.academy.max_level == 30 ? "display:none;" : "") }).append($('<div/>', { 'class': "modifier_icon research_icon research40x40 set_sail" })).append(cbx_set_sail))
                                .append($('<div/>', { 'class': "modifier", 'style': "margin-right: 5px;" }).append($('<div/>', { 'class': "modifier_icon power power_icon45x45 unit_movement_boost" })).append(cbx_unit_movement_boost))
                                .append($('<div/>', { 'class': "modifier", 'style': "margin-right: 5px;" }).append($('<div/>', { 'class': "modifier_icon building_icon40x40 lighthouse" })).append(cbx_lighthouse))
                            )
                        )
                    )
                    .append($('<br/>', { 'style': 'clear: both' }))
                    .append($('<div/>', { 'id': 'dio_radar_result', 'style': 'overflow: hidden; margin-top: 10px;' }));
            }
            DIO_Radar.windowOpen = function (_args) {
                try {
                    (uw.WM.getWindowByType(_IdS)[0]).close()
                } catch (e) { }
                uw.WF.open(_IdS, {
                    args: _args
                })
            }
            DIO_Radar.windowclose = function () {
                try {
                    (uw.WM.getWindowByType(_IdS)[0]).close()
                } catch (e) { }
            }
            // dodanie do menu
            dio.menu[1] =
            {
                'name': getTexts("Radar", "Radar"),
                'action': "DIO_Radar.windowOpen();",
                'class': 'radar'
            }
            filldiomenu()
            // ikona w menu
            $('#tpl_dio_units_list').remove()
            $('<script/>', { 'type': "text/template", 'id': "tpl_dio_units_list" }).text('' +
                '<div class="dropdown-list sandy-box js-dropdown-list" style="max-width: 240px !important;">' +
                '<div class="corner_tl"></div>' +
                '<div class="corner_tr"></div>' +
                '<div class="corner_bl"></div>' +
                '<div class="corner_br"></div>' +
                '<div class="border_t"></div>' +
                '<div class="border_b"></div>' +
                '<div class="border_l"></div>' +
                '<div class="border_r"></div>' +
                '<div class="middle"></div>' +
                '<div class="content js-dropdown-item-list">' +
                '<% var i, l = options.length, option;' +
                'for (i = 0; i < l; i++) {' +
                'option = options[i]; %>' +
                '<div class="option unit_icon40x40 <%= option.value %>" name="<%= option.value %>"></div>' +
                '<% } %>' +
                '</div>' +
                '</div>'
            ).appendTo($('head'))


            // obsługa nowych okien
            dio.initArray.push('DIO_Radar.init()');
            dio.wndArray.push(_IdS);

            DIO_Radar.init = function () {
                "use strict";
                new _dioWindowRadar();
            }
            DIO_Radar.init()
            function _dioWindowRadar() {
                var _dioWinIds = uw.require("game/windows/ids");
                _dioWinIds[_IdS.toUpperCase()] = _IdS;
                (function () {
                    "use strict";
                    var a = window.GameControllers.TabController,
                        b = window.GameModels.Progressable,
                        c = a.extend({
                            initialize: function () {
                                if (url_dev) console.log('initialize')
                                a.prototype.initialize.apply(this, arguments);
                                console.log(DATA.radar)

                                //default_timeCS = DATA.radar.default_timeCS; //RepConvTool.getSettings(RepConv.Cookie+'radar_cs', '06:00:00')
                                //default_points = parseInt(DATA.radar.default_points); //parseInt(RepConvTool.getSettings(RepConv.Cookie+'radar_points', 0))
                                this.unregisterListeners()
                                this._radarMode(),
                                    this.registerListeners(),
                                    this.render(),
                                    this._setCurrentTown(),
                                    this.registerViewComponents()
                            },
                            unregisterListeners: function () {
                                if (url_dev) console.log('initialize')
                                $.Observer(uw.GameEvents.town.town_switch)
                                    .unsubscribe('DIO_Radar_town_town_switch'),
                                    $.Observer(uw.GameEvents.dio.radar.find_btn)
                                        .unsubscribe('DIO_Radar_dio_radar_find_btn')
                                $.Observer(uw.GameEvents.dio.radar.display_towns)
                                    .unsubscribe('DIO_Radar_dio_radar_display_towns')
                            },
                            registerListeners: function () {
                                if (url_dev) console.log('registerListeners')
                                $.Observer(uw.GameEvents.town.town_switch)
                                    .subscribe('DIO_Radar_town_town_switch', this._setCurrentTown.bind(this))
                                $.Observer(uw.GameEvents.dio.radar.find_btn)
                                    .subscribe('DIO_Radar_dio_radar_find_btn', this._findTowns.bind(this))
                                $.Observer(uw.GameEvents.dio.radar.display_towns)
                                    .subscribe('DIO_Radar_dio_radar_display_towns', this._displayTowns.bind(this))
                            },
                            render: function () {
                                if (url_dev) console.log('render');
                                var opt = []
                                $.each(uw.GameData.units, function (ii, unit) {
                                    if (unit.speed > 0) {
                                        opt.push({ value: ii })
                                    }
                                })
                                this.$el.html(
                                    header()
                                );
                                if (!$('#grepodata').get(0)) $("#dio_radar").parent().after('<a id="grepodata" href="https://grepodata.com/points?world=' + WID + '" target="_blank" style="bottom: 14px; position: absolute; right: 15px;">Powered by GREPODATA</a>');
                                dd_units = $("#dio_rr_unit").dropdown({
                                    list_pos: "center",
                                    // hover: !0,
                                    type: "image",
                                    value: "colonize_ship",
                                    template: "tpl_dio_units_list",
                                    options: opt
                                }).on("dd:change:value", function (b, c, d, e, f) {
                                    $("#dio_rr_unit").toggleClass(d)
                                    $("#dio_rr_unit").toggleClass(c)
                                    setUnitSpeed()
                                })
                                $.each(getAdds().split(" "), function (i, o) {
                                    $('.dio_modifiers .modifier_icon.' + o).tooltip(dio.getTooltip(o))
                                })

                                sp_cs_lifetime = $("#dio_cs_time").spinnerHorizontal({
                                    value: default_timeCS,
                                    step: "00:30:00",
                                    max: "48:00:00",
                                    min: "00:30:00",
                                    type: "time"
                                }),
                                    sp_town_points = $("#dio_town_points").spinnerHorizontal({
                                        value: default_points,
                                        step: 500,
                                        max: 18000,
                                        min: 0
                                    }),
                                    sp_player_idle = $("#dio_player_idle").spinnerHorizontal({
                                        value: 0,
                                        step: 1,
                                        max: 999,
                                        min: 0
                                    });
                                dd_town_lists = $("#dio_town_lists").dropdown({
                                    value: 'all',
                                    options: ddCitiesList(),
                                    // disable: (rGhostAll && rGhostAll.getValue() == 'RGHOST' || __player != null),
                                    // }).on("dd:change:value", function(a, b, c) {
                                    //     that.townList()
                                });
                                activeDeactiveShowCities()
                                return this
                            },
                            reRender: function () {
                                //this.getWindowModel().hideLoading()
                            },
                            registerViewComponents: function () {
                                if (url_dev) console.log('registerViewComponents')
                            },
                            unregisterViewComponents: function () {
                                if (url_dev) console.log('unregisterViewComponents')
                                this.unregisterComponent("dio_radar_scrollbar")
                            },
                            destroy: function () {
                                if (url_dev) console.log('destroy')
                                this.unregisterViewComponents();
                                this.unregisterListeners()
                            },
                            _setCurrentTown: function () {
                                var _wnd = this.getWindowModel();
                                this.getWindowModel().showLoading();
                                setTimeout(function () {
                                    setCurrentTown();
                                    _wnd.hideLoading()
                                }, 10)
                            },
                            _findTowns: function () {
                                $.Observer(uw.GameEvents.dio.radar.find_btn)
                                    .unsubscribe('DIO_Radar_dio_radar_find_btn')
                                var _wnd = this.getWindowModel(),
                                    that = this;
                                if (!this.working) {
                                    this.getWindowModel().showLoading();
                                    setTimeout(function () {
                                        that.working = true;
                                        $('#dio_radar_result').html("");
                                        getServerData();
                                        genTownList();
                                        generateTime();
                                        displayTownListHeader();
                                        that.unregisterListeners();
                                        that.registerListeners();
                                        _wnd.hideLoading();
                                        that.working = false;
                                    }, 500)
                                }
                            },
                            registerComponent: function (a, b, c) {
                                var d = {
                                    main: this.getWindowModel().getType(),
                                    sub: c || this.getWindowModel().getIdentifier()
                                };
                                return uw.CM.register(d, a, b);
                            },
                            unregisterComponent: function (a, b) {
                                var c = {
                                    main: this.getWindowModel().getType(),
                                    sub: b || this.getWindowModel().getIdentifier()
                                };
                                uw.CM.unregister(c, a);
                            },
                            _displayTowns: function () {
                                this.getWindowModel().showLoading();
                                this.unregisterComponent("dio_radar_scrollbar");
                                displayTownList();
                                this.registerComponent("dio_radar_scrollbar",
                                    this.$el.find(".js-scrollbar-viewport").skinableScrollbar({
                                        orientation: "vertical",
                                        template: "tpl_skinable_scrollbar",
                                        skin: "narrow",
                                        disabled: !1,
                                        elements_to_scroll: this.$el.find(".js-scrollbar-content"),
                                        element_viewport: this.$el.find(".js-scrollbar-viewport"),
                                        scroll_position: 0,
                                        min_slider_size: 16
                                    })
                                );
                                this.getWindowModel().hideLoading();
                            },
                            _radarMode: function () {
                                try {
                                    var _args = this.getWindowModel().getArguments();
                                    if (_args == undefined) {
                                        setGhost()
                                    } else {
                                        if (_args.player != undefined) {
                                            setPlayer(_args.player.id, _args.player.name)
                                        } else if (_args.alliance != undefined) {
                                            setAllliance(_args.alliance.id, _args.alliance.name)
                                        } else if (_args.town != undefined) {
                                            setTown(_args.town.id, _args.town.name, _args.town.ix, _args.town.iy)
                                        }
                                    }
                                } catch (e) {
                                    setGhost()
                                }
                            },
                            toWork: false
                        });
                    window.GameViews['DiOTView_' + _IdS] = c
                })();
                (function () {
                    "use strict";
                    var a = window.GameViews,
                        b = window.GameCollections,
                        c = window.GameModels,
                        d = window.WindowFactorySettings,
                        e = uw.require("game/windows/ids"),
                        f = uw.require("game/windows/tabs"),
                        g = e[_IdS.toUpperCase()];
                    d[g] = function (b) {
                        b = b || {};
                        return uw.us.extend({
                            window_type: g,
                            minheight: 550,
                            maxheight: 570,
                            width: 975,
                            tabs: [{
                                type: f.INDEX,
                                title: 'none',
                                content_view_constructor: a['DiOTView_' + _IdS],//.RrcRTViewRadar,
                                hidden: !0
                            }],
                            max_instances: 1,
                            activepagenr: 0,
                            minimizable: !0,
                            resizable: !1,
                            title: dio.getTitle(getTexts("Radar", "Radar")),
                            /*special_buttons: {
                                help: {
                                    action: {
                                        type: "external_link",
                                        url: '#' //RepConv.Scripts_url+'module/grchowto#radar'
                                    }
                                }
                            }*/
                        }, b)
                    }
                })()
            }
        },
    };
    $(document).ready(function () { Radar.activate(); })

    /*******************************************************************************************************************************
     * Towns Sorted List
     *******************************************************************************************************************************/

    var DIO_TSL = []
    var Towns_List = {
        activate: () => {

            var imgSprites = { tsl: Home_url + "/img/dio/logo/tsl_sprite.png" }

            $('<style id="dio_Towns_List_style"> ' +
                // Icône de menu
                '.dio.tsl { background-position: -113px -80px; cursor: pointer;}' +
                // Styles pour le module
                '#dioTslGroup { width: 290px; }' +
                '#townsSortedList { height: 100%; overflow-y: auto; font-size: 11px; font-family: Verdana; font-weight: 700; }' +
                '#TSLhead { height: 30px; width: 100%; position: relative; background: url(' + imgSprites.tsl + ') 0 0 repeat-x; }' +
                '#townsSortedListDetail { height: 365px; overflow-x: hidden; overflow-y: scroll; margin-left: 5px; }' +
                '.TSLwrapper { height: 16px; width: 260px; position: absolute; top: 0; right: 0; bottom: 0; left: 0; margin: auto; }' +
                '.TSLicon { width: 18px; height: 16px; background: url(' + imgSprites.tsl + ') -44px -31px no-repeat; display: inline-block; }' +
                '#dioTslTownsList .js-scrollbar-content { padding-left: 5px; }' +
                '.TSLcityName { display: inline-block; vertical-align: top; color: #FFF; width: 224px; text-align: center; }' +
                '.TSLitem { cursor: pointer; color: #423515; line-height: 22px; position: relative; }' +
                '.TSLitem:hover { background-color: rgba(0, 0, 0, 0.1); }' +
                '.TSLitem:hover::before { content: ""; display: inline-block; border: 4px solid transparent; border-left: 7px solid #423515; padding-right: 2px; }' +
                '.TSLitem:hover::after { content: ""; display: inline-block; background: url(' + imgSprites.tsl + ') -44px -68px no-repeat; width: 15px; height: 19px; padding-right: 10px; position: absolute; right: 20px; }' +
                '.tsl_set { content: ""; display: inline-block; border: 4px solid transparent; border-left: 7px solid #423515; padding-right: 10px; background-color: rgba(0, 0, 0, 0.1); width: 313px; padding-left: 5px; }' +
                '</style>').appendTo('head');

            Towns_List.DIO_TSL();
        },
        deactivate: () => {
            if (dio.menu[3]) delete dio.menu[3]; // Supprimer la valeur avec la clé 1
            filldiomenu()
            $("dio_Towns_List_style").remove();
            DIO_TSL.windowclose()
        },
        DIO_TSL: () => {
            "use strict";

            var _IdS = 'dio_tsl';

            DIO_TSL.createWindow = function () {
                try {
                    (uw.WM.getWindowByType(_IdS)[0]).close()
                } catch (e) { }
                window.DIOtslWnd = uw.WF.open(_IdS);
            }


            // dodanie do menu
            dio.menu[3] = { 'name': getTexts("TSL", "TSL"), 'action': "DIO_TSL.createWindow();", 'class': 'tsl' }
            filldiomenu()

            dio.initArray.push('DIO_TSL.init()');
            dio.wndArray.push(_IdS);
            DIO_TSL.init = function () {
                "use strict";
                new _dioWindowTSL();
            }
            // -- okienko
            new _dioWindowTSL()
            function _dioWindowTSL() {
                "use strict";
                var _IdS = 'dio_tsl';
                var _dioWinIds = uw.require("game/windows/ids");
                _dioWinIds[_IdS.toUpperCase()] = _IdS;
                (function () {
                    "use strict";
                    var a = window.GameControllers.TabController,
                        b = window.GameModels.Progressable,
                        c = a.extend({
                            listGroup: null,
                            initialize: function (b) {
                                a.prototype.initialize.apply(this, arguments)
                                var
                                    _wnd = this.getWindowModel(),
                                    _$el = this.$el,
                                    _content = $('<div/>')
                                        .append($('<div/>', { 'style': 'padding:5px' })
                                            .append($('<div/>', { 'id': 'dioTslGroup', 'class': 'dropdown default' }))
                                            .append($('<a/>', { 'id': 'dioTslReload', 'class': "grc_reload down_big reload", 'style': "float: right; height: 22px; margin: -1px 0 1px;" })))
                                        .append($('<div/>', { 'id': 'dioTslTownsList' }))
                                this.$el.html(_content)
                                _wnd.hideLoading();

                                if (!(_wnd.getJQElement)) _wnd.getJQElement = function () { return _content; }
                                if (!(_wnd.appendContent)) _wnd.appendContent = function (a) { return _content.append(a); }
                                if (!(_wnd.setContent2)) _wnd.setContent2 = function (a) { return _content.html(a); }
                                this.initializeComponents()
                                this.renderList()
                            },
                            registerComponent: function (a, b, c) {
                                var d = {
                                    main: this.cm_context.main,
                                    sub: c || this.cm_context.sub
                                };
                                return uw.CM.register(d, a, b)
                            },
                            unregisterComponents: function (a) {
                                var b = {
                                    main: this.getMainContext(),
                                    sub: a || this.getSubContext()
                                };
                                uw.CM.unregisterSubGroup(b)
                            },
                            destroy: function () { this.unregisterComponents() },
                            close: function () { this.unregisterComponents() },
                            initializeComponents: function () {
                                var a = this.$el, that = this;
                                this.listGroup = this.registerComponent("dioTslGroup",
                                    a.find("#dioTslGroup").dropdown({
                                        value: uw.MM.getCollections().TownGroup[0].getActiveGroupId(),
                                        options: uw.MM.getCollections().TownGroup[0].getTownGroupsForDropdown(),
                                        disabled: !uw.MM.getModels().PremiumFeatures[uw.Game.player_id].isActivated("curator")
                                    }).on("dd:change:value", function (a, b, c) {
                                        that.townList()
                                    }));
                                this.registerComponent("dioTslReload", a.find("#dioTslReload").button({}).on("btn:click", function () { that.renderList(); }));
                            },
                            render: function () {
                            },
                            renderList: function () {
                                var list = this.$el.find($('#dioTslTownsList'));
                                list.html("");
                                list.append(
                                    $('<div/>', { 'id': 'TSLhead' })
                                        .append(
                                            $('<span/>', { 'class': 'TSLwrapper' })
                                                .append($('<span/>', { 'class': 'TSLicon' }))
                                                .append(
                                                    $('<span/>', { 'class': 'TSLcityName', 'style': (uw.Game.townName.length > 14) ? ('font-size: 8px;') : '', 'townid': uw.Game.townId })
                                                        .append($('<a/>', { 'class': 'gp_town_link', 'style': 'color: white', 'href': '#' + uw.MM.getModels().Town[uw.Game.townId].getLinkFragment() }).html(uw.Game.townName))
                                                )
                                                .append($('<span/>', { 'class': 'TSLicon' }))
                                        )
                                        .append($('<div/>', { 'id': 'TSLTownList' }))
                                )
                                this.townList();
                            },
                            townList: function () {
                                function calculate() {
                                    var
                                        _unitSpeed = uw.GameData.units.attack_ship.speed,
                                        _offset = 900 / uw.Game.game_speed,
                                        elCurTown = uw.MM.getModels().Town[uw.Game.townId],
                                        swapped,
                                        elTown;
                                    $.each(uw.MM.getCollections().TownGroupTown[0].getTowns(parseInt(that.listGroup.getValue())), function (idTown, elTownInGroup) {
                                        elTown = uw.MM.getModels().Town[elTownInGroup.getTownId()]
                                        if (elCurTown.getId() != elTown.getId()) {
                                            var _dist = $.toe.calc.getDistance({ 'x': elCurTown.get('abs_x'), 'y': elCurTown.get('abs_y') }, { 'x': elTown.get('abs_x'), 'y': elTown.get('abs_y') })
                                            if (_Tlist[_dist] == undefined) {
                                                _Tlist[_dist] = { 'time': 0, 'towns': [] };
                                                _Tdist.push(_dist);
                                            }
                                            _Tlist[_dist].towns.push({ "id": elTown.getId(), "name": elTown.getName() })
                                            _Tlist[_dist].timeInSec = Math.round(50 * _dist / _unitSpeed) + _offset
                                            _Tlist[_dist].time = uw.readableUnixTimestamp(_Tlist[_dist].timeInSec, 'no_offset', { with_seconds: true });
                                        }
                                    })
                                    do {
                                        swapped = false;
                                        for (var i = 0; i < _Tdist.length - 1; i++) {
                                            if (_Tdist[i] > _Tdist[i + 1]) {
                                                var temp = _Tdist[i];
                                                _Tdist[i] = _Tdist[i + 1];
                                                _Tdist[i + 1] = temp;
                                                swapped = true;
                                            }
                                        }
                                    } while (swapped);
                                }

                                var
                                    list = this.$el.find($('#dioTslTownsList')),
                                    _Tlist = {},
                                    _Tdist = [],
                                    that = this,
                                    viewport = $('<div/>', { 'style': 'height: 334px;overflow-y: hidden; overflow-x: hidden; position: relative;', 'class': 'js-scrollbar-viewport' }),
                                    content = $('<div/>', { 'class': 'js-scrollbar-content', 'style': 'width: 100%;' });
                                calculate();
                                this.$el.find($('#dioTslTownsList .js-scrollbar-viewport')).remove()
                                list.append(
                                    viewport.append(content)
                                )
                                $.each(_Tdist, function (ind, _key) {
                                    $.each(_Tlist[_key].towns, function (iiT, eeT) {
                                        content.append($('<div/>', { 'class': 'TSLitem', 'townid': eeT.id }).text(eeT.name));
                                    })
                                });
                                viewport.skinableScrollbar({
                                    orientation: "vertical",
                                    template: "tpl_skinable_scrollbar",
                                    skin: "narrow",
                                    disabled: !1,
                                    elements_to_scroll: that.$el.find(".js-scrollbar-content"),
                                    element_viewport: that.$el.find(".js-scrollbar-viewport"),
                                    scroll_position: 0,
                                    min_slider_size: 16
                                })
                                $('#dioTslTownsList .js-scrollbar-content > div[townid]').click(function () {
                                    uw.HelperTown.townSwitch($(this).attr("townid"));
                                    that.onClick(this);
                                });
                            },
                            onClick: function (that) {
                                var tsl_item = $(that).attr('townid'),
                                    prev_item = (uw.DIOtslWnd.getJQElement()).find($('.tsl_set'));
                                $(prev_item).toggleClass('tsl_set')
                                $(that).addClass('tsl_set');
                            }
                        });
                    window.GameViews['DiOView_' + _IdS] = c
                })();
                (function () {
                    "use strict";
                    var a = window.GameViews,
                        b = window.GameCollections,
                        c = window.GameModels,
                        d = window.WindowFactorySettings,
                        e = uw.require("game/windows/ids"),
                        f = uw.require("game/windows/tabs"),
                        g = e[_IdS.toUpperCase()];
                    d[g] = function (b) {
                        b = b || {};
                        return uw.us.extend({
                            window_type: g,
                            minheight: 440,
                            maxheight: 440,
                            width: 350,
                            tabs: [{
                                type: f.INDEX,
                                title: 'none',
                                content_view_constructor: a['DiOView_' + _IdS],//.RrcRTViewTSL,
                                hidden: !0
                            }],
                            max_instances: 1,
                            activepagenr: 0,
                            minimizable: !0,
                            resizable: !1,
                            title: dio.getTitle(getTexts("TSL", "TSL")),
                            /*special_buttons: {
                            help: {
                                action: {
                                    type: "external_link",
                                    url: 'module/grchowto#tsl'
                                }
                            }
                        }*/
                        }, b)
                    }
                })();
            }
        },
    };
    $(document).ready(function () { Towns_List.activate(); })

    /*******************************************************************************************************************************
     * Academy Overview
     *******************************************************************************************************************************/
    var DIO_AO = []
    var Academy_Overview = {
        activate: () => {
            $('<style id="dio_Academy_Overview_style"> ' +
                // Icône de menu
                '.dio.ao { background-position: -77px -80px; cursor: pointer;}' +
                // Styles pour le module
                '.dio_ao_bl, .dio_ao_br, .dio_ao_green, .dio_ao_gray, .dio_ao_red {float: left; height: 24px; background: url(' + Home_url + '/img/dio/logo/survey_sprite.png) no-repeat scroll 0px -39px;}' +
                '.dio_ao_bl, .dio_ao_br {width: 2px;}' +
                '.dio_ao_green, .dio_ao_gray, .dio_ao_red {width: 36px;}' +
                '.dio_ao_bl {background-position: 0px -39px;}' +
                '.dio_ao_br {background-position: -360px -39px;}' +
                '.dio_ao_green {background-position: -321px -39px;}' +
                '.dio_ao_gray {background: gray;}' +
                '.dio_ao_red {background-position: -2px -39px;}' +
                '.dio_ao_ta {font-size: 10px; float:left; padding-top: 8px; }' +
                '.dio_ao_town {width: 130px; max-width:130px; padding-left: 5px;}' +
                '.dio_ao_ap {width: 40px; max-width:40px; text-align: right; background: url(' + uw.Game.img() + '/game/academy/points_25x25.png) no-repeat;}' +
                '.dio_ao .single-progressbar .curr { font-size: 8px;}' +
                '.dio_ao .button_upgrade, .dio_ao .button_downgrade {bottom: 1px !important; right: 1px !important;}' +
                '.dio.aom {background: url(' + uw.Game.img() + '/game/academy/points_25x25.png) no-repeat;top: 4px !important; left: 4px !important;}' +
                '</style>').appendTo('head');

            Academy_Overview.DIO_AO();
        },
        deactivate: () => {
            if (dio.menu[4]) delete dio.menu[4]; // Supprimer la valeur avec la clé 1
            filldiomenu()
            $("dio_Academy_Overview_style").remove();
            DIO_AO.windowclose()
        },
        DIO_AO: () => {
            "use strict";
            const _IdS = 'dio_ao';
            let _aoMargin = 3,
                _scroll = 'dio_ao_scroll',
                _step = 598,
                _scrollVisWidth = 600,
                _greenBox = $('<div/>')
                    .append($('<div/>', { 'class': 'dio_ao_bl' }))
                    .append($('<div/>', { 'class': 'dio_ao_green' }))
                    .append($('<div/>', { 'class': 'dio_ao_br' }))
                ,
                _grayBox = $('<div/>')
                    .append($('<div/>', { 'class': 'dio_ao_bl' }))
                    .append($('<div/>', { 'class': 'dio_ao_gray' }))
                    .append($('<div/>', { 'class': 'dio_ao_br' }))
                ,
                _redBox = $('<div/>')
                    .append($('<div/>', { 'class': 'dio_ao_bl' }))
                    .append($('<div/>', { 'class': 'dio_ao_red' }))
                    .append($('<div/>', { 'class': 'dio_ao_br' }))
                ,
                _progressBars = {}
                ,
                _scrollWidth = Object.size(uw.GameData.researches) * (40 + _aoMargin * 2),
                _scrollLock = false,
                _towns = null,//MM.getCollections().Town[0],
                _researchMode = true,
                _researchQueue = {};

            function header() {
                _aoMargin = 3
                _scroll = 'dio_ao_scroll'
                _step = 598
                _scrollVisWidth = 600
                _greenBox = $('<div/>')
                    .append($('<div/>', { 'class': 'dio_ao_bl' }))
                    .append($('<div/>', { 'class': 'dio_ao_green' }))
                    .append($('<div/>', { 'class': 'dio_ao_br' }))

                _grayBox = $('<div/>')
                    .append($('<div/>', { 'class': 'dio_ao_bl' }))
                    .append($('<div/>', { 'class': 'dio_ao_gray' }))
                    .append($('<div/>', { 'class': 'dio_ao_br' }))

                _redBox = $('<div/>')
                    .append($('<div/>', { 'class': 'dio_ao_bl' }))
                    .append($('<div/>', { 'class': 'dio_ao_red' }))
                    .append($('<div/>', { 'class': 'dio_ao_br' }))

                _progressBars = {}

                _scrollWidth = Object.size(uw.GameData.researches) * (40 + _aoMargin * 2)
                _scrollLock = false
                _towns = uw.MM.getCollections().Town[0]
                _researchMode = true
                _researchQueue = {};
                let _res = $('<div/>', { 'class': _scroll }).width(_scrollWidth),
                    _hea = $('<div/>').css({ 'clear': 'both', 'height': '40px', 'padding': '0', 'width': '100%', 'border-bottom': '1px solid #000', 'background': 'url(' + uw.Game.img() + '/game/overviews/fixed_table_header_bg.jpg) repeat-x 0 0' })
                        .append($('<div/>', { 'class': 'button_arrow left' }).css({ 'position': 'absolute', 'top': '10px', 'left': '170px' })
                            .bind('click', function () {
                                if ($('.' + _scroll).position().left > 0) {
                                    $('.' + _scroll).css({ 'left': '0px' })
                                } else {
                                    if ($('.' + _scroll).position().left != 0) {
                                        $('.' + _scroll).animate({ left: '+=' + _step + 'px' }, 400)
                                    } else {
                                        $('.' + _scroll).animate({ left: '-=' + (Math.floor(_scrollWidth / _scrollVisWidth) * _step) + 'px' }, 400)
                                    }
                                }
                            })
                        )
                        .append($('<div/>').css({ 'overflow': 'hidden', 'position': 'absolute', 'left': '190px', }).width(_scrollVisWidth).append(_res))
                        .append(
                            $('<div/>', { 'class': 'button_arrow right' }).css({ 'position': 'absolute', 'top': '10px', 'right': '15px' })
                                .click(function () {
                                    if ($('.' + _scroll).position().left < (Math.floor(_scrollWidth / _scrollVisWidth) * _step * (-1)) || $('.' + _scroll).position().left > 0) $('.' + _scroll).css({ 'left': '0px' })
                                    else {
                                        if (Math.ceil(Math.abs($('.' + _scroll).position().left) / _scrollVisWidth) == Math.floor(_scrollWidth / _scrollVisWidth)) {
                                            $('.' + _scroll).animate({ left: '+=' + (Math.floor(_scrollWidth / _scrollVisWidth) * _step) + 'px' }, 400)
                                        } else {
                                            $('.' + _scroll).animate({ left: '-=' + _step + 'px' }, 400)
                                        }
                                    }
                                })
                        );
                $.each(uw.GameData.researches, function (ind, elem) {
                    _res.append(
                        $('<div/>', { 'class': 'dio_ao_unit unit research_icon research40x40 ' + uw.GameDataResearches.getResearchCssClass(ind) }).tooltip(dio.getTooltip(ind))
                    )
                })
                return _hea;
            }
            function getResearchQueue() {
                _researchQueue = {};
                if (Object.size(uw.MM.getModels().ResearchOrder) > 0) {
                    $.each(uw.MM.getModels().ResearchOrder, function (ind, ord) {
                        _researchQueue[ord.getTownId()] = _researchQueue[ord.getTownId()] || {}
                        _researchQueue[ord.getTownId()][ord.getType()] = ord;
                    })
                }
            }
            function towns(pResearch) {
                _researchMode = pResearch;
                let _list = $('<ul/>').addClass('academy').addClass("js-scrollbar-content"),
                    _hea = $('<div/>', { 'style': 'position:relative; overflow-y:hidden; min-height:485px; max-height:485px;', 'class': "js-scrollbar-viewport" }).append(_list),
                    _odd = false,
                    _Tdist = [];

                $.each(uw.MM.getCollections().TownGroupTown[0].getTowns(uw.MM.getCollections().TownGroup[0].getActiveGroupId()), function (idTown, elTownInGroup) {
                    var elTown = uw.MM.getModels().Town[elTownInGroup.getTownId()]
                    _Tdist.push({ 'id': elTown.id, 'name': elTown.getName() });
                })
                var swapped = false;
                do {
                    swapped = false;
                    for (var i = 0; i < _Tdist.length - 1; i++) {
                        if (_Tdist[i].name > _Tdist[i + 1].name) {
                            var temp = _Tdist[i];
                            _Tdist[i] = _Tdist[i + 1];
                            _Tdist[i + 1] = temp;
                            swapped = true;
                        }
                    }
                } while (swapped)
                $.each(_Tdist, function (ind, _key) {
                    _towns.forEach(function (town) {
                        if (_key.id == town.id) {
                            let _res = $('<div/>', { 'class': _scroll }).css({ 'display': 'inline-block', 'position': 'relative', 'left': '0px', }).width(Object.size(uw.GameData.researches) * (40 + _aoMargin * 2)),
                                _town = $('<li/>', { 'class': (_odd) ? "odd" : "even", 'style': 'position: relative; min-height: 29px;' });
                            getResearchQueue()
                            var a, b = uw.GameData.researches,
                                //c = MM.getCollections().ResearchOrder[0].fragments[town.id],
                                d = town.getBuildings().getBuildingLevel('academy'),
                                e = availablePoints(town.id),
                                f = town.getResearches(),
                                g = (_researchQueue && _researchQueue[town.id] && Object.size(_researchQueue[town.id]) == uw.GameDataConstructionQueue.getResearchOrdersQueueLength()) || false;

                            _town
                                .append($('<div/>', { 'class': "dio_ao_ta dio_ao_town" }).append($('<a/>', { 'class': 'gp_town_link', 'href': town.getLinkFragment(), 'rel': town.id }).html(town.getName())))
                                .append($('<div/>', { 'class': "dio_ao_ta dio_ao_ap", 'id': 'dio_ao_' + town.id }).html(e))
                                .append($('<div/>').css({ 'overflow': 'hidden', 'position': 'absolute', 'left': (190 - _aoMargin * 2) + 'px', 'top': '3px', }).width(_scrollVisWidth).append(_res))

                            $.each(uw.GameData.researches, function (ind, elem) {
                                var h = b[ind],
                                    i = f.hasResearch(ind),
                                    j = (_researchQueue && _researchQueue[town.id] && Object.size(_researchQueue[town.id]) == uw.GameDataConstructionQueue.getResearchOrdersQueueLength()) || false,
                                    det = fillBox(town.id, ind),
                                    _btn = getBtn(town.id, ind);
                                _res.append(
                                    $('<div/>', {
                                        'class': 'textbox tech_tree_box ' + ind,
                                        'id': 'dio_ao_' + town.id + '_' + ind
                                    })
                                        .data('town', town.id)
                                        .append(det)
                                        .append(_btn)
                                        .hover(function () { $(this).find($('.button_downgrade,.button_upgrade')).slideDown() }, function () { $(this).find($('.button_downgrade,.button_upgrade')).slideUp() })
                                        .tooltip(
                                            (_researchMode || (!_researchMode && !i && !j)) ?
                                                uw.DiOAcademyTooltipFactory.getResearchTooltip(h, d, e, i, j, g, town.id) :
                                                uw.AcademyTooltipFactory.getRevertTooltip(h, uw.MM.checkAndPublishRawModel('Player', { id: uw.Game.player_id }).getCulturalPoints())
                                        )
                                )
                            })
                            _odd = !_odd
                            _list.append(_town)
                        }
                    })
                });
                return _hea;
            }

            function availablePoints(townId) {
                var town = uw.MM.getCollections().Town[0].get(townId),
                    _maxPoints = (town.getBuildings().getBuildingLevel('academy') * uw.GameDataResearches.getResearchPointsPerAcademyLevel())
                        + (town.getBuildings().getBuildingLevel('library') * uw.GameDataResearches.getResearchPointsPerLibraryLevel()),
                    _availablePoints = _maxPoints,
                    _townRes = town.getResources()
                $.each(uw.GameData.researches, function (ind, elem) {
                    if (town.getResearches().get(ind)) {
                        _availablePoints -= elem.research_points;
                    }
                })
                getResearchQueue();
                if (Object.size(_researchQueue) > 0 && _researchQueue[townId]) {
                    $.each(_researchQueue[townId], function (iRO, _ord) {
                        _availablePoints -= uw.GameData.researches[iRO].research_points
                    })
                }
                if (url_dev) console.log(_availablePoints);
                return _availablePoints;
            }
            function fillBox(townId, research) {
                if (url_dev) console.log('wypelnienie dla town_id [' + townId + '] => ' + research);
                let town = _towns.get(townId), _green = town.getResearches().get(research), _result;
                if (uw.GameData.researches[research].building_dependencies.academy <= town.getBuildings().getBuildingLevel('academy')) {
                    if (_researchQueue && _researchQueue[town.id] && _researchQueue[town.id][research]) {
                        var _ord = _researchQueue[town.id][research];
                        if (_ord.getType() == research) {
                            _progressBars[townId + '_' + research] = $('<div/>', { 'class': "single-progressbar instant_buy js-item-progressbar type_unit_queue" })
                                .singleProgressbar({
                                    template: "tpl_pb_single_nomax",
                                    type: "time",
                                    reverse_progress: !0,
                                    liveprogress: !0,
                                    liveprogress_interval: 1,
                                    value: _ord.getRealTimeLeft(),
                                    max: _ord.getDuration(),
                                    countdown: !0,
                                }).on("pb:cd:finish", function () {
                                    $(this).parent().html(_greenBox.html())
                                    this.destroy()
                                })
                            _result = _progressBars[townId + '_' + research];
                        }
                        return _result || _greenBox.html();
                    } else {
                        return ((_green) ? _greenBox.html() : _redBox.html());
                    }
                } else {
                    return _grayBox.html();
                }
            }
            function getBtn(townId, research) {
                var
                    town = _towns.get(townId),
                    _green = town.getResearches().get(research),
                    _result;
                if (uw.GameData.researches[research].building_dependencies.academy <= town.getBuildings().getBuildingLevel('academy')) {
                    if (_researchQueue && _researchQueue[town.id] && _researchQueue[town.id][research]) {
                        return '';
                    } else {
                        if (!_green && _researchMode) {
                            _result = $('<div/>', { 'class': "btn_upgrade button_upgrade" })
                                .hide()
                                .data('town_id', townId)
                                .data('research', research)
                                .click(function () {
                                    var
                                        townId = $(this).data('town_id'),
                                        research = $(this).data('research');
                                    if (url_dev) console.log(townId + ' => ' + research);
                                    uw.gpAjax.ajaxPost("frontend_bridge", "execute", {
                                        "model_url": "ResearchOrder",
                                        "action_name": "research",
                                        "arguments": { "id": research },
                                        "town_id": townId
                                    }, !0, {
                                        success: function (h, i) {
                                            getResearchQueue();
                                            $('#dio_ao_' + townId + '_' + research).html(fillBox(townId, research));
                                            $('#dio_ao_' + townId).html(availablePoints(townId));
                                        },
                                        error: function (a, b) {
                                            if (url_dev) console.log(a)
                                            if (url_dev) console.log(b)
                                        }
                                    })
                                });
                        } else if (_green && !_researchMode) {
                            _result = $('<div/>', { 'class': "btn_downgrade button_downgrade" })
                                .hide()
                                .data('town_id', townId)
                                .data('research', research)
                                .click(function () {
                                    var btn = this;
                                    uw.ConfirmationWindowFactory.openConfirmationResettingResearch(function (btn) {
                                        var
                                            townId = $(btn).data('town_id'),
                                            research = $(btn).data('research');
                                        if (url_dev) console.log('Potwierdzenie dla: ' + townId + ' => ' + research);
                                        uw.gpAjax.ajaxPost("frontend_bridge", "execute", {
                                            "model_url": "ResearchOrder",
                                            "action_name": "revert",
                                            "arguments": { "id": research },
                                            "town_id": townId
                                        }, !0, {
                                            success: function (h, i) {
                                                getResearchQueue();
                                                $('#dio_ao_' + townId + '_' + research).html(fillBox(townId, research));
                                                $('#dio_ao_' + townId).html(availablePoints(townId));
                                            },
                                            error: function (a, b) {
                                                if (url_dev) console.log(a)
                                                if (url_dev) console.log(b)
                                            }
                                        })
                                    }.bind(btn, this))
                                });
                        }
                    }
                }
                return _result;
            }
            function getActiveGroupName() {
                var _res = '';
                uw.MM.getCollections().TownGroup[0].forEach(function (group) {
                    if (group.getId() == uw.MM.getCollections().TownGroup[0].getActiveGroupId()) {
                        _res = " (" + group.getName() + ")";
                    }
                })
                return _res;
            }

            // dodanie do menu
            dio.menu[4] = { 'name': getTexts("AO", "AO"), 'action': "DIO_AO.windowOpen();", 'class': 'aom' }
            filldiomenu()

            $('head').append($('<style/>')
                .append('.dio_ao_unit { margin: 0 ' + _aoMargin + 'px !important;}')
                .append('.' + _scroll + ' {display: inline-block; position: relative; left: 0px;}')
                .append('.dio_ao_scroll .textbox {margin: 0px ' + _aoMargin + 'px; width: 40px; float: left;}')
            )

            DIO_AO.windowOpen = function () {
                try {
                    (uw.WM.getWindowByType(_IdS)[0]).close()
                } catch (e) { }
                uw.WF.open(_IdS)
            }
            // definicja okna
            dio.initArray.push('DIO_AO.init()');
            dio.wndArray.push(_IdS);
            DIO_AO.init = function () {
                "use strict";
                _towns = uw.MM.getCollections().Town[0]
                _scrollWidth = Object.size(uw.GameData.researches) * (40 + _aoMargin * 2);
                new _DiOGameDataResearches(window);
                new _DiOAcademyTooltipFactory();
                new _dioWindowAO();
            }
            DIO_AO.init()
            function _dioWindowAO() {
                "use strict";
                var _IdS = 'dio_ao';
                var _dioWinIds = uw.require("game/windows/ids");
                _dioWinIds[_IdS.toUpperCase()] = _IdS;
                (function () {
                    "use strict";
                    var a = window.GameControllers.TabController,
                        b = window.GameModels.Progressable,
                        _content = $('<div/>', { 'id': 'townsoverview' }),
                        c = a.extend({
                            initialize: function (b) {
                                if (url_dev) console.time("initialize");
                                a.prototype.initialize.apply(this, arguments)
                                var
                                    _wnd = this.getWindowModel(),
                                    _$el = this.$el;//.css({'margin':'10px'});
                                this.$el.html(_content)
                                _wnd.hideLoading();
                                if (!(_wnd.getJQElement)) _wnd.getJQElement = function () { return _content; }
                                if (!(_wnd.appendContent)) _wnd.appendContent = function (a) { return _content.append(a); }
                                if (!(_wnd.setContent2)) _wnd.setContent2 = function (a) { return _content.html(a); }
                                this.bindEventListeners()
                                if (url_dev) console.timeEnd("initialize");
                            },
                            render: function () {
                                this.reRender()
                            },
                            reRender: function () {
                                if (url_dev) console.time("reRender");
                                var
                                    _wnd = this.getWindowModel(),
                                    _$el = this.$el;
                                this.getWindowModel().setTitle(dio.getTitle(uw.GameData.buildings.academy.name + getActiveGroupName()))
                                uw.MM.getCollections().TownGroup[0].getTownGroups()
                                this.getWindowModel().showLoading()
                                setTimeout(function () {
                                    if (url_dev) console.time("fill");
                                    _wnd.setContent2(header())
                                    _wnd.appendContent(towns(_wnd.getActivePageNr() == 0))
                                    _wnd.hideLoading()
                                    if (url_dev) console.timeEnd("fill");
                                    _$el.find(".js-scrollbar-viewport").skinableScrollbar({
                                        orientation: "vertical",
                                        template: "tpl_skinable_scrollbar",
                                        skin: "narrow",
                                        disabled: !1,
                                        elements_to_scroll: _$el.find(".js-scrollbar-content"),
                                        element_viewport: _$el.find(".js-scrollbar-viewport"),
                                        scroll_position: 0,
                                        min_slider_size: 16
                                    })
                                }, 100)
                                if (url_dev) console.timeEnd("reRender");
                            },
                            bindEventListeners: function () {
                                this.$el.parents('.' + _IdS).on("click", ".js-wnd-buttons .help", this._handleHelpButtonClickEvent.bind(this))
                            },
                            _handleHelpButtonClickEvent: function () {
                                var a = this.getWindowModel().getHelpButtonSettings();
                                uw.RepConvGRC.openDIO(a.action.tab, a.action.args);
                            }
                        });
                    //window.GameViews.RrcRTViewTSL = c
                    window.GameViews['DiOView_' + _IdS] = c
                })();
                (function () {
                    "use strict";
                    var a = window.GameViews,
                        b = window.GameCollections,
                        c = window.GameModels,
                        d = window.WindowFactorySettings,
                        e = uw.require("game/windows/ids"),
                        f = uw.require("game/windows/tabs"),
                        g = e[_IdS.toUpperCase()];
                    d[g] = function (b) {
                        b = b || {};
                        var c = uw.DM.getl10n(e.ACADEMY);
                        return uw.us.extend({
                            window_type: g,
                            minheight: 570,
                            maxheight: 580,
                            width: 822,
                            tabs: [{
                                type: f.RESEARCH,
                                title: c.tabs[0],
                                content_view_constructor: a['DiOView_' + _IdS],
                                hidden: !1
                            }, {
                                type: f.RESET,
                                title: c.tabs[1],
                                content_view_constructor: a['DiOView_' + _IdS],
                                hidden: !1
                            }],
                            max_instances: 1,
                            activepagenr: 0,
                            title: dio.getTitle(uw.GameData.buildings.academy.name)
                        }, b)
                    }
                })();
            }

            function _DiOAcademyTooltipFactory() {
                "use strict";

                function a(a) { return '<img src="' + uw.Game.img() + "/game/res/" + ("population" === a ? "pop" : a) + '.png" alt="' + e[a] + '" />' }

                function b(a) { return '<p style="width: 320px;">' + a.description + "</p>" }

                function c(b, c, e, townId) {
                    let i = "";
                    const j = {},
                        k = uw.ITowns.getTown(townId),
                        l = k.resources(),
                        m = k.getProduction(),
                        result = {
                            upgrade_not_possible: false,
                            enough_resources: true,
                            time_to_build: 0
                        };

                    const r = d(b, c, townId);

                    for (let f in r) {
                        if (r.hasOwnProperty(f)) {
                            const g = r[f];
                            i += a(f);

                            if (f === "research_points" && g.amount > e) {
                                result.upgrade_not_possible = true;
                                result.enough_resources = false;
                            }

                            if (g.amount > l[f]) {
                                result.upgrade_not_possible = true;

                                if (f !== "time" && f !== "research_points") {
                                    result.enough_resources = false;

                                    if (m[f] > 0) {
                                        const h = parseInt(3600 * parseFloat((g.amount - l[f]) / m[f]), 10);
                                        if (h > result.time_to_build && h > 0) {
                                            result.time_to_build = h;
                                        }
                                    }
                                }
                            }

                            if (f === "time") g.amount = uw.DateHelper.readableSeconds(g.amount);
                            const colorStyle = (g.amount > l[f] || (f === "research_points" && !result.enough_resources)) ? ' style="color:#B00"' : "";
                            i += `<span${colorStyle}>${g.amount}</span>`;
                        }
                    }
                    result.result = i;
                    return result;
                }

                function d(a, b, townId) {
                    var c = uw.DiOGameDataResearches.getResearchCosts(a, townId);
                    //console.log(a, townId)
                    return {
                        wood: { amount: Math.floor(c.wood, 10) },
                        stone: { amount: Math.floor(c.stone, 10) },
                        iron: { amount: Math.floor(c.iron, 10) },
                        research_points: { amount: a.research_points },
                        time: { amount: uw.GameDataResearches.getResearchTime(a, b) }
                    }
                }
                function s(e) { var i; if (!e) return ""; for (i = 1; i < arguments.length; i++)e = e.split("%" + i).join(arguments[i]); return e }
                var e = uw.DM.getl10n("tooltips", "academy"),
                    f = {
                        getResearchTooltip: function (a, d, f, g, h, i, townId) {
                            var j = "";
                            j += '<div class="academy_popup">';
                            j += "<h4>" + a.name + "</h4>";
                            j += b(a);

                            if (g) j += "<h5>" + e.already_researched + "</h5>";
                            else if (h) j += "<h5>" + e.in_progress + "</h5>";
                            else {
                                var k = c(a, d, f, townId);
                                j += k.result + "<br/>";
                                var l = a.building_dependencies;
                                if (d < l.academy) {
                                    j += "<h5>" + e.building_dependencies + "</h5>";
                                    j += '<span class="requirement">' + uw.GameData.buildings.academy.name + " " + l.academy + "</span><br />";
                                }
                                if (!k.enough_resources) j += '<span class="requirement">' + e.not_enough_resources + '</span><br /><span class="requirement">' + s(e.enough_resources_in, uw.DateHelper.formatDateTimeNice(Timestamp.server() + k.time_to_build, !1)) + "</span><br />";
                                if (i) j += '<span class="requirement">' + e.full_queue + "</span><br />"
                            }
                            j += "</div>"
                            return j
                        }
                    };
                window.DiOAcademyTooltipFactory = f
            }


            function _DiOGameDataResearches(a) {
                "use strict";
                var b = {
                    getResearchCostsById: function (a, townId) {
                        var b = uw.GameData.researches[a];
                        return this.getResearchCosts(b, townId)
                    },
                    getResearchCosts: function (a, townId) {
                        if (!(uw.MM.getCollections().PlayerHero[0])) { uw.MM.createBackboneObjects({ PlayerHeroes: null }, window.GameCollections, {}) }
                        var b = a.resources, c = uw.GeneralModifications.getResearchResourcesModification(townId);
                        return {
                            wood: Math.ceil(b.wood * c),
                            stone: Math.ceil(b.stone * c),
                            iron: Math.ceil(b.iron * c)
                        };
                    }
                },
                    c = $.extend({}, uw.GameDataResearches, b);
                a.DiOGameDataResearches = c
            }
        },
    };
    $(document).ready(function () { Academy_Overview.activate(); })