---
title: Método IWMPNetwork setProxyExceptionList
description: El método setProxyExceptionList especifica la lista de excepciones de proxy. | Método IWMPNetwork setProxyExceptionList
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- Método setProxyExceptionList Reproductor de Windows Media
- Método setProxyExceptionList Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , método setProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddfd3ce8495c02fc6ae352f918349ff7174afb99e69d9e1ba8aa19c45d1a49d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745767"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a>IWMPNetwork::setProxyExceptionList (método)

El **método setProxyExceptionList** especifica la lista de excepciones de proxy.

## <a name="syntax"></a>Sintaxis


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrProtocol* \[ En\]
</dt> <dd>

**System.String que** es el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> <dt>

*pbstrExceptionList* \[ En\]
</dt> <dd>

**System.String que** es una lista delimitada por punto y coma de hosts para los que se omite el servidor proxy. Los espacios iniciales y finales no deben estar presentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se trata de una lista de equipos, dominios o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.

El \* carácter se puede usar como carácter comodín para enumerar entradas. Por ejemplo, .com coincidiría con todos los hosts del dominio com, mientras que 67. coincidiría con todos los hosts de la subred de la \* \* clase A 67.

Este método no tiene ningún efecto a menos que el valor recuperado de **IWMPNetwork.getProxySettings** sea 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa setProxyExceptionList para** especificar una lista de hosts para los que se omite el servidor proxy cuando se usa el protocolo MMS. La nueva lista se recupera de un cuadro de texto cuando se hace clic en un botón. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxyExceptionList (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





