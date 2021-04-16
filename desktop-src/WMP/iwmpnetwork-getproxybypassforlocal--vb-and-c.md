---
title: IWMPNetwork getProxyBypassForLocal, método
description: El método getProxyBypassForLocal devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- método getProxyBypassForLocal de Windows Media Player
- método getProxyBypassForLocal Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690366"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a>IWMPNetwork:: getProxyBypassForLocal (método)

El método **getProxyBypassForLocal** devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrProtocol* 
</dt> <dd>

**System. String** que es el nombre del protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor **System. Boolean** que indica si se omite el servidor proxy. El valor solo es significativo cuando **IWMPNetwork. getProxySettings** devuelve un valor de 2 (use la configuración manual).

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se usa **getProxyBypassForLocal** para mostrar si Windows Media Player está establecido para omitir el servidor proxy para las direcciones locales. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|-----------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                             |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                         |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxyBypassForLocal (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





