---
title: Método remove de IWMPMediaCollection
description: El método remove quita un elemento especificado de la colección de medios.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- remove method Reproductor de Windows Media
- Remove method Reproductor de Windows Media , IWMPMediaCollection (interfaz)
- Interfaz IWMPMediaCollection Reproductor de Windows Media , método remove
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359261"
---
# <a name="iwmpmediacollectionremove-method"></a>IWMPMediaCollection::remove (método)

El `remove` método quita un elemento especificado de la colección de medios.

## <a name="syntax"></a>Sintaxis


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItem* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPMedia** que identifica el elemento que se quitará.

</dd> <dt>

*varfDeleteFile* \[ En\]
</dt> <dd>

Valor **System.Boolean** que especifica si el método debe quitar el elemento especificado de la biblioteca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método elimina un elemento de la biblioteca. Este método no elimina archivos del equipo del usuario.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente, después de preguntar al usuario, se elimina permanentemente el primer elemento multimedia de la colección de medios mediante `remove` . El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.add (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





