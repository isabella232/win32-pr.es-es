---
title: Propiedad IWMPCdrom Playlist
description: La propiedad Lista de reproducción obtiene una interfaz IWMPPlaylist que representa las pistas del CD actualmente en la unidad de CD o las entradas de título de nivel raíz de un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propiedad de lista de reproducción Reproductor de Windows Media
- Propiedad de lista Reproductor de Windows Media lista de reproducción, interfaz IWMPCdrom
- Interfaz IWMPCdrom Reproductor de Windows Media , propiedad Playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579377"
---
# <a name="iwmpcdromplaylist-property"></a>Propiedad IWMPCdrom::P laylist

La **propiedad Lista** de reproducción obtiene una interfaz **IWMPPlaylist** que representa las pistas del CD actualmente en la unidad de CD o las entradas de título de nivel raíz de un DVD.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Valor de propiedad

Interfaz **WMPLib.IWMPPlaylist.**

## <a name="remarks"></a>Observaciones

Normalmente, el contenido basado en DVD se organiza en títulos. Cada título contiene uno o varios capítulos. Cada DVD se ha escrito de forma diferente, por lo que la forma en que se usan los títulos y los capítulos es cosa del autor del contenido.

Para un DVD, esta propiedad obtiene una lista de reproducción que contiene como primer elemento una **interfaz IWMPMedia** denominada "DVD". Esta interfaz representa los medios de DVD. La reproducción del elemento da como resultado que el DVD se reproduce desde el principio si es la primera reproducción después de insertar un DVD nuevo o reanudar la reproducción si el DVD es el mismo que el último DVD visto. Al establecer este elemento como el elemento actual durante la reproducción, se reproduce el DVD desde el principio.

Los elementos adicionales (representados por interfaces **IWMPMedia)** en la lista de reproducción son títulos de DVD representados por listas de reproducción anidadas. Al establecer **IWMPControls.currentItem** en igual a uno de estos elementos de lista de reproducción anidados, Reproductor de Windows Media establece automáticamente la lista de reproducción anidada como la lista de reproducción actual después de que comience la reproducción del capítulo. A continuación, puede usar las propiedades de interfaz **IWMPPlaylist,** los métodos y los eventos asociados para trabajar con capítulos de DVD, que también son elementos de lista de reproducción.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa Lista** de reproducción para rellenar un cuadro de texto de varias líneas, denominado myText, con la lista de pistas del CD de audio actualmente en la primera unidad de CD. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdrom (VB y C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





