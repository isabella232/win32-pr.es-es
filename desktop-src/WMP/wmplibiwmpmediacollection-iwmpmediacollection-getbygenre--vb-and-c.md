---
title: Método IWMPMediaCollection getByGenre
description: El método getByGenre devuelve una interfaz IWMPPlaylist que proporciona acceso a elementos multimedia del género especificado.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- Método getByGenre Reproductor de Windows Media
- Método getByGenre Reproductor de Windows Media , interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Reproductor de Windows Media , método getByGenre
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172697"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>IWMPMediaCollection::getByGenre (método)

El `getByGenre` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia del género especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrGenre* \[ En\]
</dt> <dd>

**System.String que** es el nombre del género.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para los elementos multimedia recuperados.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del método depende de cuál de esas dos maneras `getByGenre` se use. Si recupera la interfaz llamando a [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el método devuelve todos los elementos multimedia `getByGenre` de la biblioteca. Sin embargo, si recupera la interfaz mediante una llamada a [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el método devuelve solo los elementos de audio de la biblioteca que tienen el atributo y el valor `getByGenre` especificados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se `getByGenre` usa para recuperar una lista de reproducción de elementos multimedia cuando el usuario hace clic en un botón. La lista de reproducción contiene elementos con el género especificado por el usuario en un cuadro de texto. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

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

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





