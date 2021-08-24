---
title: Método IWMPCdromCollection Item
description: El método Item devuelve una interfaz IWMPCdrom en el índice especificado.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Método item Reproductor de Windows Media
- Método item Reproductor de Windows Media , interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection Reproductor de Windows Media método , Item
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ab1ced32918e615230b3267d15dfbe5b2ba28377f6bbf265b735ea666153a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900115"
---
# <a name="iwmpcdromcollectionitem-method"></a>IWMPCdromCollection::Item (Método)

El **método Item** devuelve una interfaz **IWMPCdrom** en el índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* \[ En\]
</dt> <dd>

**System.Int32** que es el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPCdrom.**

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa Item** para mostrar el especificador de unidad y el nombre de la lista de reproducción de cada CD disponible en el equipo en un cuadro de lista. Si la unidad realmente contiene contenido de DVD, Windows XP o posterior. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdrom (VB y C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection (VB y C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection.count (VB y C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection.getByDriveSpecifier (VB y C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.name (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





