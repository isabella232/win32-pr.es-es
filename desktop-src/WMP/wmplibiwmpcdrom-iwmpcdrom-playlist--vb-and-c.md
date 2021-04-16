---
title: Propiedad de lista de reproducción IWMPCdrom
description: La propiedad playlist obtiene una interfaz IWMPPlaylist que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propiedades de la lista de reproducción Windows Media Player
- Propiedad de lista de reproducción Windows Media Player, interfaz IWMPCdrom
- Interfaz IWMPCdrom Windows Media Player, propiedad playlist
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718845"
---
# <a name="iwmpcdromplaylist-property"></a>IWMPCdrom::P propiedad laylist

La propiedad **playlist** obtiene una interfaz **IWMPPlaylist** que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de un DVD.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Valor de propiedad

Una interfaz **WMPLib. IWMPPlaylist** .

## <a name="remarks"></a>Observaciones

Normalmente, el contenido basado en DVD se organiza en títulos. Cada título contiene uno o varios capítulos. Cada DVD se crea de forma diferente, por lo que la forma de usar títulos y capítulos depende del autor del contenido.

En un DVD, esta propiedad obtiene una lista de reproducción que contiene como primer elemento una interfaz **IWMPMedia** denominada "DVD". Esta interfaz representa el medio DVD. Reproducir el elemento hace que el DVD se reproduzca desde el principio si es el primer juego después de insertar un DVD nuevo o reanudar la reproducción si el DVD es el mismo que el último DVD visualizado. Al establecer este elemento como el elemento actual durante la reproducción, el DVD se reproduce desde el principio.

Los elementos adicionales (representados por las interfaces **IWMPMedia** ) de la lista de reproducción son títulos de DVD que se representan mediante listas de reproducción anidadas. Al establecer **IWMPControls. CurrentItem** en uno de estos elementos de lista de reproducción anidados, Windows Media Player establece automáticamente la lista de reproducción anidada como la lista de reproducción actual después de que comience la reproducción del capítulo. A continuación, puede usar las propiedades, los métodos y los eventos asociados de la interfaz **IWMPPlaylist** para trabajar con capítulos de DVD, que también son elementos de lista de reproducción.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la lista de **reproducción** para rellenar un cuadro de texto de varias líneas, denominado mi texto, con la lista de seguimiento del CD de audio que se encuentra en la primera unidad de CD. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


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
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdrom (VB y C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





