---
title: IWMPMediaCollection setDeleted, método
description: El método setDeleted mueve el elemento multimedia especificado a la carpeta elementos eliminados. | IWMPMediaCollection setDeleted, método
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- método setDeleted de Windows Media Player
- método setDeleted Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método setDeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700334"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>IWMPMediaCollection:: setDeleted (método)

El `setDeleted` método mueve el elemento multimedia especificado a la carpeta elementos eliminados.

## <a name="syntax"></a>Sintaxis


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItem* \[ de\]
</dt> <dd>

Una interfaz **WMPLib. IWMPMedia** para el elemento que se va a desplace.

</dd> <dt>

*varfIsDeleted* \[ de\]
</dt> <dd>

Valor **System. Boolean** que especifica si el elemento debe moverse a la carpeta de elementos eliminados. Este valor siempre debe ser **true**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método no quita los archivos del equipo del usuario, simplemente los mueve a la carpeta elementos eliminados.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente `setDeleted` se usa para trasladar un elemento multimedia determinado a la carpeta elementos eliminados. El método **IsDeleted** comprueba primero si el elemento ya se ha eliminado. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
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

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





