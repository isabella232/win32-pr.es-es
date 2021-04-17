---
title: IWMPMedia setItemInfo, método
description: El método setItemInfo establece el valor del atributo especificado para el elemento multimedia.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670916"
---
# <a name="iwmpmediasetiteminfo-method"></a>IWMPMedia:: setItemInfo (método)

El método **setItemInfo** establece el valor del atributo especificado para el elemento multimedia.

## <a name="syntax"></a>Sintaxis


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItemName* \[ de\]
</dt> <dd>

**System. String** que es el nombre del atributo.

</dd> <dt>

*bstrVal* \[ de\]
</dt> <dd>

**System. String** que es el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La propiedad **attributeCount** obtiene el número de atributos disponibles para un elemento multimedia determinado. Los números de índice se pueden usar con el método **getAttributeName** para determinar los nombres de los atributos integrados que se pueden usar con este método.

Antes de usar este método, utilice el método **isReadOnlyItem** para detectar si un atributo determinado se puede establecer.

Antes de llamar a este método, debe tener acceso total a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Nota

Si incrusta el control Media Player de Windows en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Media Player de Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **setItemInfo** para cambiar el valor del atributo Genre del elemento multimedia actual. Un cuadro de texto permite al usuario escribir una cadena, que se utiliza para cambiar la información del atributo en respuesta al evento de clic de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. isReadOnlyItem (VB y C#)**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





