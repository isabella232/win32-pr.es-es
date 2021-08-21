---
title: Método IWMPNetwork getProxyExceptionList
description: El método getProxyExceptionList devuelve la lista de excepciones de proxy.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- Método getProxyExceptionList Reproductor de Windows Media
- Método getProxyExceptionList Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , método getProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96434d4ea2341a8d33fcb9673898f4adca5eae7ace27eb7a7cafb9d482d74a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053543"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a>IWMPNetwork::getProxyExceptionList (método)

El **método getProxyExceptionList** devuelve la lista de excepciones de proxy.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrProtocol* \[ En\]
</dt> <dd>

**System.String que** es el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es una lista delimitada por punto y coma de hosts para los que se omite el servidor proxy. El valor solo es significativo cuando **IWMPNetwork.getProxySettings** devuelve un valor de 2 (use la configuración manual).

## <a name="remarks"></a>Comentarios

Se trata de una lista de equipos, dominios o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.

El \* carácter se puede usar como carácter comodín para enumerar entradas. Por ejemplo, .com coincidiría con todos los hosts del dominio com, mientras que 67. coincidiría con todos los hosts de la subred de la \* \* clase A 67.

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa getProxyExceptionList** para mostrar si Reproductor de Windows Media está establecido para omitir el servidor proxy para las direcciones locales. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxyExceptionList (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





