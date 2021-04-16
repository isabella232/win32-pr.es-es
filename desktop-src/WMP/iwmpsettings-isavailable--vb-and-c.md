---
title: IWMPSettings. isAvailable (VB y C)
description: La propiedad isAvailable (el \_ método get isavailable en C \) obtiene un valor que indica si se puede realizar una acción especificada.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. isAvailable (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699322"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="19936-104">IWMPSettings. isAvailable (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="19936-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="19936-105">La propiedad **isavailable** (el método **Get \_ isavailable** en C#) obtiene un valor que indica si se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="19936-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="19936-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19936-106">Parameters</span></span>

<span data-ttu-id="19936-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="19936-107">*bstrItem*</span></span>

<span data-ttu-id="19936-108">**System. String** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="19936-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="19936-109">Value</span><span class="sxs-lookup"><span data-stu-id="19936-109">Value</span></span>              | <span data-ttu-id="19936-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="19936-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19936-111">AutoStart</span><span class="sxs-lookup"><span data-stu-id="19936-111">AutoStart</span></span>          | <span data-ttu-id="19936-112">Detecta si la propiedad autoStart se puede establecer para especificar que Windows Media Player inicia la reproducción automáticamente.</span><span class="sxs-lookup"><span data-stu-id="19936-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="19936-113">Saldo</span><span class="sxs-lookup"><span data-stu-id="19936-113">Balance</span></span>            | <span data-ttu-id="19936-114">Detecta si la propiedad de saldo se puede usar para establecer el equilibrio estéreo.</span><span class="sxs-lookup"><span data-stu-id="19936-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="19936-115">BaseURL</span><span class="sxs-lookup"><span data-stu-id="19936-115">BaseURL</span></span>            | <span data-ttu-id="19936-116">Detecta si la propiedad baseURL se puede establecer para especificar una dirección URL base.</span><span class="sxs-lookup"><span data-stu-id="19936-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="19936-117">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="19936-117">DefaultFrame</span></span>       | <span data-ttu-id="19936-118">Detecta si la propiedad defaultFrame se puede establecer para especificar el marco predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19936-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="19936-119">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="19936-119">EnableErrorDialogs</span></span> | <span data-ttu-id="19936-120">Detecta si la propiedad enableErrorDialogs se puede establecer para habilitar o deshabilitar la visualización de cuadros de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="19936-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="19936-121">GetMode</span><span class="sxs-lookup"><span data-stu-id="19936-121">GetMode</span></span>            | <span data-ttu-id="19936-122">Detecta si el método getMode se puede usar para recuperar el bucle actual o el modo de orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="19936-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="19936-123">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="19936-123">InvokeURLs</span></span>         | <span data-ttu-id="19936-124">Detecta si la propiedad invokeURLs se puede establecer para especificar si los eventos de dirección URL deben iniciar un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="19936-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="19936-125">Silencio</span><span class="sxs-lookup"><span data-stu-id="19936-125">Mute</span></span>               | <span data-ttu-id="19936-126">Detecta si la propiedad silenciar se puede establecer para especificar si la salida de audio está activada o desactivada.</span><span class="sxs-lookup"><span data-stu-id="19936-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="19936-127">PlayCount</span><span class="sxs-lookup"><span data-stu-id="19936-127">PlayCount</span></span>          | <span data-ttu-id="19936-128">Detecta si la propiedad playCount se puede establecer para especificar el número de veces que se reproducirá un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="19936-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="19936-129">Tarifa</span><span class="sxs-lookup"><span data-stu-id="19936-129">Rate</span></span>               | <span data-ttu-id="19936-130">Detecta si la propiedad Rate se puede establecer para controlar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="19936-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="19936-131">SetMode</span><span class="sxs-lookup"><span data-stu-id="19936-131">SetMode</span></span>            | <span data-ttu-id="19936-132">Detecta si el método setMode se puede usar para especificar el bucle actual o el modo de orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="19936-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="19936-133">Volumen</span><span class="sxs-lookup"><span data-stu-id="19936-133">Volume</span></span>             | <span data-ttu-id="19936-134">Detecta si la propiedad de volumen se puede establecer para especificar el volumen de audio.</span><span class="sxs-lookup"><span data-stu-id="19936-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="19936-135">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="19936-135">Property Value</span></span>

<span data-ttu-id="19936-136">Un valor **System. Boolean** que indica si se puede realizar la acción especificada.</span><span class="sxs-lookup"><span data-stu-id="19936-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="19936-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19936-137">Remarks</span></span>

<span data-ttu-id="19936-138">**IWMPSettings. isIdentical** es una propiedad de Visual Basic que toma un parámetro.</span><span class="sxs-lookup"><span data-stu-id="19936-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="19936-139">En C#, se hace referencia a él como el método **IWMPSettings. Get \_ isIdentical** .</span><span class="sxs-lookup"><span data-stu-id="19936-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="19936-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="19936-140">Examples</span></span>

<span data-ttu-id="19936-141">En el ejemplo siguiente se prueba cada una de las propiedades de **IWMPSettings** mediante la propiedad **isavailable** (el método **Get \_ isavailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="19936-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="19936-142">El nombre de la propiedad y el resultado de cada prueba se muestran en un cuadro de texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="19936-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="19936-143">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="19936-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="19936-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19936-144">Requirements</span></span>



| <span data-ttu-id="19936-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="19936-145">Requirement</span></span> | <span data-ttu-id="19936-146">Value</span><span class="sxs-lookup"><span data-stu-id="19936-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19936-147">Versión</span><span class="sxs-lookup"><span data-stu-id="19936-147">Version</span></span><br/>   | <span data-ttu-id="19936-148">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="19936-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="19936-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19936-149">Namespace</span></span><br/> | <span data-ttu-id="19936-150">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="19936-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="19936-151">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="19936-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="19936-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="19936-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19936-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="19936-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19936-154">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-155">**IWMPSettings. autoStart (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-156">**IWMPSettings. balance (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-157">**IWMPSettings. baseURL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-158">**IWMPSettings. defaultFrame (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-159">**IWMPSettings. enableErrorDialogs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-160">**IWMPSettings. getMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-161">**IWMPSettings. invokeURLs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-162">**IWMPSettings. MUTE (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-163">**IWMPSettings. playCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-164">**IWMPSettings. Rate (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-165">**IWMPSettings. setMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19936-166">**IWMPSettings. VOLUME (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="19936-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





