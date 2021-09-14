---
title: Método getProxySettings de IWMPNetwork
description: El método getProxySettings devuelve información sobre la configuración de proxy de un protocolo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Método getProxySettings Reproductor de Windows Media
- Método getProxySettings Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , método getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264700"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>IWMPNetwork::getProxySettings (método)

El **método getProxySettings** devuelve información sobre la configuración de proxy de un protocolo.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrProtocol* \[ En\]
</dt> <dd>

**System.String que** es el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Int32** que es uno de los valores siguientes.



| Value | Descripción                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | No se usa un servidor proxy.                                                |
| 1     | Se usa la configuración de proxy para el explorador actual (válido solo para HTTP). |
| 2     | Se usa la configuración de proxy especificada manualmente.                            |
| 3     | La configuración del proxy se detecta automáticamente.                                      |



 

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa getProxySettings** para mostrar un mensaje, que proporciona información sobre la configuración de proxy actual del reproductor, en una etiqueta. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxySettings (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





