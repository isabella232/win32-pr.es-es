---
title: Implementación de CEchoPropPage Apply
description: Implementación de CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, método CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903559"
---
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="49f36-109">Implementación de CEchoPropPage:: Apply</span><span class="sxs-lookup"><span data-stu-id="49f36-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="49f36-110">El método CEchoPropPage:: Apply se implementa en EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="49f36-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="49f36-111">Se ejecuta cuando el usuario hace clic en **aplicar** en el cuadro de diálogo Página de propiedades de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="49f36-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="49f36-112">El código de ejemplo del Asistente para complementos proporciona una implementación para controlar una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="49f36-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="49f36-113">Puede modificar este código para una de las propiedades de ejemplo de eco y, a continuación, agregar código para almacenar el otro valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="49f36-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="49f36-114">Declarar las variables de método Apply</span><span class="sxs-lookup"><span data-stu-id="49f36-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="49f36-115">En primer lugar, debe quitar la declaración de fScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="49f36-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="49f36-116">A continuación, agregue las declaraciones de variable que necesitará.</span><span class="sxs-lookup"><span data-stu-id="49f36-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="49f36-117">En el ejemplo siguiente se muestran las declaraciones de variables completadas:</span><span class="sxs-lookup"><span data-stu-id="49f36-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="49f36-118">Recuperación de los valores de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="49f36-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="49f36-119">Debe implementar el código para recuperar y validar los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="49f36-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="49f36-120">En el ejemplo de código siguiente se recupera el valor de tiempo de retraso del \_ cuadro de edición IDC DELAYTIME y, a continuación, se comprueba si el valor está dentro de un intervalo especificado:</span><span class="sxs-lookup"><span data-stu-id="49f36-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



<span data-ttu-id="49f36-121">Si la entrada del usuario no está en el intervalo especificado, el código muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="49f36-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="49f36-122">Observe el uso del recurso de cadena que creó anteriormente para el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="49f36-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="49f36-123">En el ejemplo siguiente se recupera el nivel de efecto del \_ cuadro de edición IDC WETMIX y, a continuación, se comprueba que el valor está dentro de un intervalo especificado:</span><span class="sxs-lookup"><span data-stu-id="49f36-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="49f36-124">Almacenar los valores de propiedad en el registro</span><span class="sxs-lookup"><span data-stu-id="49f36-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="49f36-125">A continuación, el código debe conservar los nuevos valores de propiedad en el registro.</span><span class="sxs-lookup"><span data-stu-id="49f36-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="49f36-126">El código siguiente almacena ambos valores de propiedad:</span><span class="sxs-lookup"><span data-stu-id="49f36-126">The following code stores both property values:</span></span>


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="49f36-127">Actualizar los valores de las propiedades de los complementos de eco</span><span class="sxs-lookup"><span data-stu-id="49f36-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="49f36-128">El método **Apply** debe informar al complemento echo de que los valores de propiedad han cambiado.</span><span class="sxs-lookup"><span data-stu-id="49f36-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="49f36-129">El código siguiente llama al método put de propiedad para cada propiedad mediante el puntero de interfaz recuperado en CEchoPropPage:: SetObjects:</span><span class="sxs-lookup"><span data-stu-id="49f36-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



<span data-ttu-id="49f36-130">Observe que el valor de la combinación húmeda se convierte en el punto flotante antes de pasarse al complemento.</span><span class="sxs-lookup"><span data-stu-id="49f36-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="49f36-131">Deshabilitar el botón aplicar</span><span class="sxs-lookup"><span data-stu-id="49f36-131">Disabling the Apply Button</span></span>

<span data-ttu-id="49f36-132">Como paso final, el código debe deshabilitar aplicar en el cuadro de diálogo Página de propiedades como una señal al usuario de que los valores se han actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="49f36-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="49f36-133">Esto requiere la siguiente línea de código:</span><span class="sxs-lookup"><span data-stu-id="49f36-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="49f36-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49f36-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f36-135">**Modificar la página de propiedades de ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="49f36-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




