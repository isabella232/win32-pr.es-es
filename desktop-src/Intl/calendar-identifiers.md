---
description: En este tema se definen los identificadores de calendario (tipo de datos CALID) que se usan para especificar calendarios diferentes.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificadores de calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f9f21aeff1143c4f981e3bfae20214f1b86e86307f7f32b103a19ef99b9803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083035"
---
# <a name="calendar-identifiers"></a>Identificadores de calendario

En este tema se definen los identificadores de calendario (tipo de datos CALID) que se usan para especificar calendarios diferentes. Las aplicaciones pueden usar estos identificadores al usar las siguientes funciones NLS y funciones de devolución de llamada, que tienen parámetros que toman el tipo de datos CALID:

-   [**ConvertSystemTimeToCalDateTime**](convertsystemtimetocaldatetime.md)
-   [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**GetCalendarSupportedDateRange**](getcalendarsupporteddaterange.md)
-   [**IsCalendarLeapYear**](iscalendarleapyear.md)
-   [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Se definen los valores siguientes. Todos los demás valores están reservados. Estos valores no se pueden combinar entre sí.



Identificador de calendario

Significado

1

CAL \_ GREGORIAN

Gregoriano (localizado)

2

CAL \_ GREGORIANO \_ EE. UU.

Gregoriano (cadenas en inglés siempre)

3

CAL \_ JAPAN

Era del japonés

4

CAL \_ TAIWAN

Calendario de Taiwán

5

CAL \_ KOREA

Tangun coreano era

6

CAL \_ HIJRI

Hijri (lunar árabe)

7

CAL \_ TAILANDÉS

Tailandés

8

CAL \_ HEBREO

Hebreo (Lunar)

9

CAL \_ GREGORIAN \_ ME \_ FRENCH

Gregorian Middle East French

10

ÁRABE \_ CAL \_ GREGORIANO

Gregorian Arabic

11

CAL \_ GREGORIAN \_ XLIT \_ ENGLISH

Inglés transliterado gregoriano

12

CAL \_ GREGORIAN \_ XLIT \_ FRENCH

Francés transliterado gregoriano

23

CAL \_ UMALQURA

**Windows Vista y versiones posteriores:** Calendario Um Al Arabica (lunar árabe)



 

> [!Note]  
> La brecha en la numeración entre los identificadores CAL \_ GREGORIAN \_ XLIT \_ FRENCH y CAL \_ UMALQURA es intencionada. El designador para CAL \_ UMALQURA es 23, no 13.

 

Además, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) y [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permiten el uso del valor ENUM ALL CALENDARS para solicitar una enumeración de todos los \_ \_ calendarios aplicables.

Value

Significado

0xffffffff

ENUMERAR \_ TODOS \_ LOS CALENDARIOS

Todos los calendarios aplicables para la configuración regional especificada



 

 

 
