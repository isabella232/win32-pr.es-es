---
title: Cómo procesar la notificación de DTN_FORMAT notificación
description: En este tema se muestra cómo procesar una notificación de formato enviada por el control selector de fecha y hora (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167641"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Cómo procesar la notificación DTN \_ FORMAT

En este tema se muestra cómo procesar una notificación de formato enviada por el control selector de fecha y hora (DTP).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instrucciones


Un control DTP envía la [notificación DTN \_ FORMAT](dtn-format.md) para solicitar texto que se mostrará en un campo de devolución de llamada del control. La aplicación debe controlar esta notificación para permitir que el control DTP muestre información que no admite de forma nativa.

El siguiente ejemplo de código de C++ es una función definida por la aplicación (**DoFormat**) que procesa códigos de [notificación \_ DTN FORMAT](dtn-format.md) proporcionando una cadena de texto para un campo de devolución de llamada. La aplicación llama a la función definida por la aplicación **GetDayNum** para solicitar el número de día que se usará en la cadena de devolución de llamada.


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



**Función definida por la aplicación GetDayNum**

La función de ejemplo Definida por la aplicación **DoFormat** llama a la siguiente función definida por la aplicación **GetDayNum** para solicitar el número de día en función de la fecha actual. **GetDayNum devuelve** un valor **INT** que representa el día actual del año, de 0 a 366. Esta función llama a otra función definida por la aplicación, **IsLeapYr,** durante el procesamiento.


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



**Función definida por la aplicación IsLeapYr**

La función definida por la aplicación **GetDayNum** llama a la función **IsLeapYr** para determinar si el año actual es un año bisiesco. **IsLeapYr devuelve** un **valor BOOL** que es **TRUE** si es un año bisiesco y **FALSE** en caso contrario.


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
}        
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles selectores de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia del control selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




