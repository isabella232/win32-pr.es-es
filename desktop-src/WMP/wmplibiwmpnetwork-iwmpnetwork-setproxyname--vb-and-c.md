---
title: IWMPNetwork setProxyName, método
description: El método setProxyName especifica el nombre del servidor proxy que se va a usar. | IWMPNetwork setProxyName, método
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- método setProxyName de Windows Media Player
- método setProxyName Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método setProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650204"
---
# <a name="iwmpnetworksetproxyname-method"></a>IWMPNetwork:: setProxyName (método)

El método **setProxyName** especifica el nombre del servidor proxy que se va a usar.

## <a name="syntax"></a>Sintaxis


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrProtocol* \[ de\]
</dt> <dd>

**System. String** que es el nombre del protocolo. Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).

</dd> <dt>

*bstrProxyName* \[ de\]
</dt> <dd>

**System. String** que es el nombre del servidor proxy que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método no tiene ningún efecto a menos que el valor recuperado de **IWMPNetwork. getProxySettings** es 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se usa **setProxyName** para especificar el nombre del servidor proxy de Windows Media Player para el protocolo MMS. El nuevo nombre se recupera de un cuadro de texto cuando se hace clic en un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxyName (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





