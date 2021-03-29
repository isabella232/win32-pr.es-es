---
title: Cómo procesar la notificación de DTN_FORMAT
description: En este tema se muestra cómo procesar una notificación de formato enviada por el control selector de fecha y hora (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904905"
---
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="16076-103">Cómo procesar la notificación de \_ formato DTN</span><span class="sxs-lookup"><span data-stu-id="16076-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="16076-104">En este tema se muestra cómo procesar una notificación de formato enviada por el control selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="16076-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="16076-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="16076-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="16076-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="16076-106">Technologies</span></span>

-   [<span data-ttu-id="16076-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="16076-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="16076-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16076-108">Prerequisites</span></span>

-   <span data-ttu-id="16076-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="16076-109">C/C++</span></span>
-   <span data-ttu-id="16076-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="16076-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="16076-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="16076-111">Instructions</span></span>


<span data-ttu-id="16076-112">Un control de DTP envía la notificación de [ \_ formato DTN](dtn-format.md) al texto de la solicitud que se mostrará en un campo de devolución de llamada del control.</span><span class="sxs-lookup"><span data-stu-id="16076-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="16076-113">La aplicación debe controlar esta notificación para permitir que el control de DTP muestre información que no admite de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="16076-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="16076-114">El siguiente ejemplo de código C++ es una función definida por la aplicación (**OnFormat**) que procesa los códigos de notificación de [ \_ formato DTN](dtn-format.md) proporcionando una cadena de texto para un campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="16076-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="16076-115">La aplicación llama a la función definida por la aplicación **GetDayNum** para solicitar el número de días que se va a usar en la cadena de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="16076-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


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



<span data-ttu-id="16076-116">**La función definida por la aplicación GetDayNum**</span><span class="sxs-lookup"><span data-stu-id="16076-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="16076-117">La función de ejemplo definida por la aplicación **OnFormat** llama a la siguiente función definida por la aplicación **GetDayNum** para solicitar el número de días basándose en la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="16076-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="16076-118">**GetDayNum** devuelve un valor **int** que representa el día actual del año, de 0 a 366.</span><span class="sxs-lookup"><span data-stu-id="16076-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="16076-119">Esta función llama a otra función definida por la aplicación, **IsLeapYr**, durante el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="16076-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


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



<span data-ttu-id="16076-120">**La función definida por la aplicación IsLeapYr**</span><span class="sxs-lookup"><span data-stu-id="16076-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="16076-121">La función definida por la aplicación **GetDayNum** llama a la función **IsLeapYr** para determinar si el año actual es un año bisiesto.</span><span class="sxs-lookup"><span data-stu-id="16076-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="16076-122">**IsLeapYr** devuelve un valor **booleano** que es **true** si es un año bisiesto y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="16076-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="16076-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16076-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16076-124">Usar controles de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="16076-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="16076-125">Referencia de control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="16076-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="16076-126">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="16076-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




