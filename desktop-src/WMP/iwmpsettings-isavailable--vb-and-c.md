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
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings. isAvailable (VB y C#)

La propiedad **isavailable** (el método **Get \_ isavailable** en C#) obtiene un valor que indica si se puede realizar una acción especificada.


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



## <a name="parameters"></a>Parámetros

*bstrItem*

**System. String** que es uno de los valores siguientes.



| Value              | Descripción                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| AutoStart          | Detecta si la propiedad autoStart se puede establecer para especificar que Windows Media Player inicia la reproducción automáticamente. |
| Saldo            | Detecta si la propiedad de saldo se puede usar para establecer el equilibrio estéreo.                                           |
| BaseURL            | Detecta si la propiedad baseURL se puede establecer para especificar una dirección URL base.                                                |
| DefaultFrame       | Detecta si la propiedad defaultFrame se puede establecer para especificar el marco predeterminado.                                    |
| EnableErrorDialogs | Detecta si la propiedad enableErrorDialogs se puede establecer para habilitar o deshabilitar la visualización de cuadros de diálogo de error.        |
| GetMode            | Detecta si el método getMode se puede usar para recuperar el bucle actual o el modo de orden aleatorio.                          |
| InvokeURLs         | Detecta si la propiedad invokeURLs se puede establecer para especificar si los eventos de dirección URL deben iniciar un explorador Web.         |
| Silencio               | Detecta si la propiedad silenciar se puede establecer para especificar si la salida de audio está activada o desactivada.                        |
| PlayCount          | Detecta si la propiedad playCount se puede establecer para especificar el número de veces que se reproducirá un elemento multimedia.                 |
| Tarifa               | Detecta si la propiedad Rate se puede establecer para controlar la velocidad de reproducción.                                            |
| SetMode            | Detecta si el método setMode se puede usar para especificar el bucle actual o el modo de orden aleatorio.                           |
| Volumen             | Detecta si la propiedad de volumen se puede establecer para especificar el volumen de audio.                                           |



 

## <a name="property-value"></a>Valor de propiedad

Un valor **System. Boolean** que indica si se puede realizar la acción especificada.

## <a name="remarks"></a>Observaciones

**IWMPSettings. isIdentical** es una propiedad de Visual Basic que toma un parámetro. En C#, se hace referencia a él como el método **IWMPSettings. Get \_ isIdentical** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se prueba cada una de las propiedades de **IWMPSettings** mediante la propiedad **isavailable** (el método **Get \_ isavailable** en C#). El nombre de la propiedad y el resultado de cada prueba se muestran en un cuadro de texto de varias líneas. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


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





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autoStart (VB y C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. balance (VB y C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB y C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB y C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. getMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. MUTE (VB y C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. playCount (VB y C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. VOLUME (VB y C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





