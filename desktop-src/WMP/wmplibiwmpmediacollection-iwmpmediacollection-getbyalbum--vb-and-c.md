---
title: IWMPMediaCollection getByAlbum, método
description: El método getByAlbum devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia del álbum especificado.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- método getByAlbum de Windows Media Player
- método getByAlbum Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671813"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a>IWMPMediaCollection:: getByAlbum (método)

El método **getByAlbum** devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia del álbum especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAlbum* \[ de\]
</dt> <dd>

**System. String** que es el título del álbum.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPPlaylist** para los elementos multimedia recuperados.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del método **getByAlbum** depende de cuál de esas dos maneras se usa. Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el método **getByAlbum** devuelve todos los elementos multimedia de la biblioteca. Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el método **getByAlbum** devuelve solo los elementos de audio de la biblioteca que pertenecen al álbum especificado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **getByAlbum** para crear una lista de reproducción de elementos multimedia cuando el usuario hace clic en un botón. La lista de reproducción contiene elementos con el álbum especificado por el usuario en un cuadro de texto. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

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

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





