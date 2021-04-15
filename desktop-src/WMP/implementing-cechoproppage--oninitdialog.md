---
title: Implementación de CEchoPropPage OnInitDialog
description: Implementación de CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, CEchoPropPage OnInitDialog (método)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695260"
---
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="eccb6-109">Implementar CEchoPropPage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="eccb6-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="eccb6-110">El método **CEchoPropPage:: OnInitDialog** se implementa en EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="eccb6-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="eccb6-111">Se ejecuta cuando se invoca el cuadro de diálogo de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="eccb6-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="eccb6-112">El código de este método debe recuperar los valores de propiedad actuales y mostrarlos en el cuadro de edición correcto.</span><span class="sxs-lookup"><span data-stu-id="eccb6-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="eccb6-113">El código de ejemplo del Asistente para complementos proporciona una implementación para una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="eccb6-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="eccb6-114">Puede modificar este código para una de las propiedades de ejemplo de eco y, a continuación, agregar código para recuperar el segundo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="eccb6-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="eccb6-115">Declarar las variables del método OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="eccb6-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="eccb6-116">En primer lugar, debe quitar la declaración de fScaleFactor y reemplazarla por las siguientes declaraciones de variable:</span><span class="sxs-lookup"><span data-stu-id="eccb6-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="eccb6-117">Recuperar los valores actuales del complemento</span><span class="sxs-lookup"><span data-stu-id="eccb6-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="eccb6-118">El código debe intentar después recuperar los valores de propiedad actuales del complemento de eco.</span><span class="sxs-lookup"><span data-stu-id="eccb6-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="eccb6-119">En el ejemplo siguiente se intenta recuperar cada propiedad:</span><span class="sxs-lookup"><span data-stu-id="eccb6-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="eccb6-120">En el cuadro de diálogo se muestra el valor de nivel de efectos para el usuario como un entero, pero el complemento almacena el valor como un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eccb6-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="eccb6-121">Por lo tanto, el código convierte el valor de punto flotante en un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="eccb6-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="eccb6-122">Recuperación de los valores actuales del registro</span><span class="sxs-lookup"><span data-stu-id="eccb6-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="eccb6-123">Si la página de propiedades no puede recuperar los valores actuales del complemento, debe intentar leerlos desde el registro.</span><span class="sxs-lookup"><span data-stu-id="eccb6-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="eccb6-124">El código siguiente lee cada valor de propiedad:</span><span class="sxs-lookup"><span data-stu-id="eccb6-124">The following code reads each property value:</span></span>


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



<span data-ttu-id="eccb6-125">Observe el uso de las constantes del registro que creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="eccb6-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="eccb6-126">Mostrar los valores al usuario</span><span class="sxs-lookup"><span data-stu-id="eccb6-126">Displaying the Values to the User</span></span>

<span data-ttu-id="eccb6-127">Por último, la página de propiedades debe mostrar los valores en los controles de cuadro de edición correctos.</span><span class="sxs-lookup"><span data-stu-id="eccb6-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="eccb6-128">En el código de ejemplo siguiente se muestra esto:</span><span class="sxs-lookup"><span data-stu-id="eccb6-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="eccb6-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eccb6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eccb6-130">**Modificar la página de propiedades de ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="eccb6-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




