---
name: ww-input-date-time-picker
description: >-
  The `ww-input-date-time-picker` component provides a versatile and
  configurable interface for selecting single or multiple dates and times,
  supporting various display formats, locales, and selection modes to
  accommodate diverse user needs.
keywords:
  - date/time picker
  - date range selection
  - time selection
  - multi-date selection
  - locale support
  - timezone configuration
  - 24-hour format
  - custom day names
  - range mode
  - flow feature
---

#### ww-input-date-time-picker

1. **Component Purpose:** This component renders a date/time picker with various configurations and options. It allows users to select a single date, a date range, or multiple dates, with additional features like time selection, month/year selection, and more.

2. **Properties:**
   - `formatedValue`: `string | Date | [Date, Date?] | Date[]` - The current value of the date picker. This is a computed property based on the `variableValue`.
   - `readonly`: `boolean | null` - Whether the input is read-only. Default: `false`.
   - `required`: `boolean` - Whether the input is required. Default: `false`.
   - `previewFormat`: `string | null` - The format to display the selected date(s) in the preview. Default: `null`.
   - `locale`: `string` - The locale to use for the date picker. Default: `wwLib.wwLang.lang`.
   - `formatLocale`: `object` - The locale object used by date-fns for formatting dates.
   - `timezone`: `string | null` - The timezone to use for the date picker. Default: `null`.
   - `dpKey`: `string` - A unique key used to force re-render the date picker component.
   - `modelType`: `"yyyy-MM-dd" | "HH:mm:SS" | "yyyy-MM" | null` - The model type for the selected date(s).
   - `isReadOnly`: `boolean` - Whether the input is read-only, determined by the `readonly` prop and the component's state.
   - `customDayNames`: `string[] | null` - Custom day names to display in the calendar, based on the `locale` prop.
   - `selectionMode`: `"single" | "range" | "multi"` - The selection mode for the date picker. Default: `"single"`.
   - `initValueSingle`: `string | null` - The initial value for the single selection mode.
   - `initValueRangeStart`: `string | null` - The initial start value for the range selection mode.
   - `initValueRangeEnd`: `string | null` - The initial end value for the range selection mode.
   - `initValueMulti`: `string[] | null` - The initial values for the multi-date selection mode.
   - `multiDatesLimit`: `number` - The maximum number of dates that can be selected in multi-date mode. Default: `0` (unlimited).
   - `rangeMode`: `"free" | "auto" | "minmax"` - The range mode for the date picker when in range selection mode. Default: `"free"`.
   - `enablePartialRange`: `boolean` - Whether to allow partial range selection in free range mode. Default: `true`.
   - `autoRange`: `number` - The number of days to automatically select when in auto range mode. Default: `1`.
   - `minRange`: `number` - The minimum number of days in the range when in minmax range mode. Default: `2`.
   - `maxRange`: `number` - The maximum number of days in the range when in minmax range mode. Default: `7`.
   - `noDisabledRange`: `boolean` - Whether to disable the disabled range feature for range selection. Default: `false`.
   - `dateMode`: `"datetime" | "date" | "time" | "month" | "year"` - The date/time mode for the date picker. Default: `"datetime"`.
   - `enableSeconds`: `boolean` - Whether to enable seconds selection in time mode. Default: `false`.
   - `use24`: `boolean` - Whether to use 24-hour format for time selection. Default: `false`.
   - `enableMultiCalendars`: `boolean` - Whether to enable multiple calendars in range selection mode. Default: `false`.
   - `multiCalendars`: `number` - The number of calendars to display when `enableMultiCalendars` is `true`. Default: `2`.
   - `multiCalendarsSolo`: `boolean` - Whether the multiple calendars should be independent or linked. Default: `false`.
   - `orientation`: `"horizontal" | "vertical"` - The orientation of the date picker. Default: `"horizontal"`.
   - `hideOffsetDates`: `boolean` - Whether to hide offset dates in the calendar. Default: `false`.
   - `disableMonthYearSelect`: `boolean` - Whether to disable the month/year selection. Default: `false`.
   - `startDate`: `string | null` - The start date for the date picker. Default: `null`.
   - `minDate`: `string | null` - The minimum date that can be selected. Default: `null`.
   - `maxDate`: `string | null` - The maximum date that can be selected. Default: `null`.
   - `preventMinMaxNavigation`: `boolean` - Whether to prevent navigation beyond the minimum and maximum dates. Default: `false`.
   - `ignoreTimeValidation`: `boolean` - Whether to ignore time validation. Default: `false`.
   - `allowedDates`: `string[]` - An array of allowed dates in the date picker. Default: `[]`.
   - `disabledDates`: `string[]` - An array of disabled dates in the date picker. Default: `[]`.
   - `disabledWeekDays`: `string[]` - An array of disabled week days in the date picker. Default: `[]`.
   - `weekStart`: `"0" | "1" | "2" | "3" | "4" | "5" | "6"` - The day to start the week on. Default: `"1"` (Monday).
   - `weekNumbers`: `"none" | "local" | "iso"` - Whether to display week numbers, and in what format. Default: `"none"`.
   - `autoApply`: `boolean` - Whether to automatically apply the selected date(s) when valid. Default: `false`.
   - `closeOnAutoApply`: `boolean` - Whether to close the date picker when automatically applying the selected date(s). Default: `true`.
   - `enableFlow`: `boolean` - Whether to enable the flow feature for selecting date/time components. Default: `false`.
   - `flowSteps`: `string[]` - The order of steps in the flow. Default: `["month", "year", "calendar", "time", "minutes", "hours", "seconds"]`.

3. **Children Components:**

   - `triggerZone`: `any[]` -  An array of objects representing the trigger zone for the date picker. Generally a flexbox acting like a button.
   - `actionSelectElement`: An object representing the "Select" button in the action row.

4. **Example:**

   {
      "tag": "ww-input-date-time-picker",
      "name": "Date & Time picker",
      "props": {"default":{"lang":"pageLang","use24":false,"format":"MMM D, YYYY","maxDate":"","minDate":"","dateMode":"datetime","maxRange":7,"minRange":2,"readonly":false,"timezone":"locale","autoApply":true,"autoRange":1,"flowSteps":["month","year","calendar","time","minutes","hours","seconds"],"rangeMode":"free","startDate":"2025-01-07T00:00:00.000Z","weekStart":"1","enableFlow":false,"orientation":"horizontal","weekNumbers":"none","customFormat":"","menuPosition":"center","advancedDates":true,"closeOnScroll":false,"enableSeconds":false,"selectionMode":"single","themeCellSize":"35px","themeFontSize":"16px","advancedColors":false,"advancedStyles":false,"multiCalendars":2,"themeIconColor":"#959595","themeTextColor":"#212121","calendarOnlyFit":"stretch","hideOffsetDates":false,"multiDatesLimit":0,"noDisabledRange":false,"themeHoverColor":"#f3f3f3","closeOnAutoApply":true,"themeBorderColor":"#ddd","themeCellPadding":"5px","themeDangerColor":"#ff6f60","enableLeftSidebar":false,"themeBorderRadius":"4px","themeMenuMinWidth":"250px","themePrimaryColor":"#1976d2","themeSuccessColor":"#76d275","themeTimeFontSize":"32px","enableCalendarOnly":false,"enablePartialRange":false,"enableRightSidebar":false,"multiCalendarsSolo":false,"themeDisabledColor":"#f6f6f6","themeHighlightColor":"#1976d219","themeHoverIconColor":"#959595","themeHoverTextColor":"#212121","themeScrollBarColor":"#959595","themeSecondaryColor":"#c0c4cc","enableMultiCalendars":false,"ignoreTimeValidation":false,"themeBackgroundColor":"#ffffff","themeMenuBorderColor":"#ddd","themePreviewFontSize":"13px","themeBorderHoverColor":"#aaaeb7","themeCellBorderRadius":"4px","themePrimaryTextColor":"#f8f5f5","disableMonthYearSelect":false,"preventMinMaxNavigation":false,"themeSuccessDisabledColor":"#a3d9b1","themeScrollBarBackgroundColor":"#f3f3f3","required":false}},
      "styles": {"default":{"border":"1px solid #d1d5db","cursor":"pointer","padding":"0px 0px"}},
      "children": {
         "triggerZone": [
            {
               "tag": "ww-flexbox",
               "name": "Placeholder container",
               "styles": {"default":{"display":"flex","width":"100%","height":"38px","padding":"0 12px","flexWrap":true,"alignItems":"center","flexDirection":"row","justifyContent":"space-between"}},
               "children": {
               "children": [
                  {
                     "tag": "ww-text",
                     "name": "Placeholder",
                     "settings": {"name":"Date input"},
                     "props": {"default":{"tag":"p","text":{"en":{"code":"context.item.data['preview']||\"Select a date\"","__wwtype":"f","defaultValue":"<div>Select a date</div>"}}}},
                     "styles": {"default":{"fontSize":"16px","wordSpacing":"0px","letterSpacing":"0px","textDecoration":"none","textDecorationStyle":"solid"}}
                  },
                  {
                     "tag": "ww-icon",
                     "props": {"default":{"icon":"icon-calendar","color":"#6E6E6E","fontSize":24}},
                     "styles": {"default":{"width":"max-content","height":"auto","padding":"0px","transform":"translate3d(0px,0px,0px) rotateX(0deg) rotateY(0deg) rotateZ(0deg)","borderRadius":"auto"}}
                  }
               ]
               }
            }
         ],
         "actionSelectElement": {
            "tag": "ww-button",
            "name": "Select button",
            "settings": {"name":"Select button"},
            "props": {"default":{"disabled":false,"buttonType":"button","text":"Select"}},
            "styles": {"default":{"fontSize":"16px","fontWeight":"initial","wordSpacing":"0px","letterSpacing":"0px","textTransform":"none","textDecoration":"none","textDecorationStyle":"solid"}}
         }
      }
   }

Important: Height of the input have to be set on triggerZone ww-flexbox styles, not in root ww-input-date-time-picker styles.