---
description: En este tema se definen los identificadores de calendario (tipo de datos CALID) que se usan para especificar calendarios diferentes.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificadores de calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809517"
---
# <a name="calendar-identifiers"></a>Identificadores de calendario

En este tema se definen los identificadores de calendario (tipo de datos CALID) que se usan para especificar calendarios diferentes. Las aplicaciones pueden utilizar estos identificadores al usar las siguientes funciones NLS y funciones de devolución de llamada, que tienen parámetros que toman el tipo de datos CALID:

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

\_calendario gregoriano

Gregoriano (localizado)

2

CAL \_ gregoriano \_

Gregoriano (cadenas en inglés siempre)

3

CAL \_ Japón

Era del Emperador japonés

4

CAL \_ Taiwán

Calendario taiwanés

5

CAL \_ Corea

Coreano Tangun era

6

HIJRI de CAL \_

Hijri (Árabe lunar)

7

CAL \_ tailandés

Tailandés

8

hebreo de CAL \_

Hebreo (lunar)

9

\_calendario gregoriano \_ \_ francés de cal

Gregorian Middle East French

10

CAL \_ gregoriano \_ Árabe

Gregorian Arabic

11

CAL \_ gregoriano \_ XLIT \_ Inglés

Gregoriano (transliteración) Inglés

12

CAL \_ gregoriano \_ XLIT \_ Francés

Gregoriano (transliteración) francés

23

CAL \_ UMALQURA

**Windows Vista y versiones posteriores:** Calendario de Um al-Qura (Árabe lunar)



 

> [!Note]  
> El intervalo de numeración entre los identificadores CAL \_ gregoriano \_ XLIT \_ francés y cal \_ UMALQURA es intencionado. El designador de CAL \_ UMALQURA es 23, no 13.

 

Además, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) y [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permiten el uso del valor enumerar \_ todos los \_ calendarios para solicitar una enumeración de todos los calendarios aplicables.

Value

Significado

0xFFFFFFFF

ENUMERAr \_ todos los \_ calendarios

Todos los calendarios aplicables para la configuración regional especificada



 

 

 
