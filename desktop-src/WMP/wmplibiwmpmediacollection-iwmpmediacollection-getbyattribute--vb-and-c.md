---
title: Método getByAttribute de IWMPMediaCollection
description: El método getByAttribute devuelve una interfaz IWMPPlaylist que corresponde al atributo especificado que tiene el valor especificado.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- Método getByAttribute Reproductor de Windows Media
- Método getByAttribute Reproductor de Windows Media , interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Reproductor de Windows Media , método getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172705"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>IWMPMediaCollection::getByAttribute (método)

El **método getByAttribute** devuelve una **interfaz IWMPPlaylist** que corresponde al atributo especificado que tiene el valor especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribute* \[ En\]
</dt> <dd>

**System.String que** es el atributo especificado.

</dd> <dt>

*bstrValue* \[ En\]
</dt> <dd>

**System.String que** es el valor especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para los elementos multimedia recuperados.

## <a name="remarks"></a>Observaciones

Este método se puede usar para crear una consulta genérica para elementos multimedia que coincidan con un valor para un atributo de la biblioteca. Esto es útil en el caso de los atributos definidos por el usuario. Si el atributo no existe, se producirá un error.

Puede usar este método para recuperar todos los elementos multimedia de un tipo específico. Use el nombre de atributo **MediaType** y uno de los valores siguientes.



| Value    | Descripción                                               |
|----------|-----------------------------------------------------------|
| audio    | Música y otros elementos de solo audio                          |
| otro    | Otros elementos, como un archivo .asf o la dirección URL de una secuencia. |
| Foto    | Elementos de foto. Requiere Reproductor de Windows Media 10.            |
| Reproducción | Listas de reproducción representadas como elementos multimedia.                     |
| radio    | Elementos de estación de radio. No lo usa Reproductor de Windows Media 10. |
| video    | Elementos de vídeo.                                              |



 

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la [Referencia de atributos](attribute-reference.md).

Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del método **getByAttribute** depende de cuál de esas dos maneras se use. Si recupera la interfaz mediante una llamada a [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el **método getByAttribute** devuelve todos los elementos multimedia de la biblioteca. Sin embargo, si recupera la interfaz mediante una llamada a [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el método **getByAttribute** devuelve solo los elementos de audio de la biblioteca que tienen el atributo y el valor especificados.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa getByAttribute para** reproducir todo el contenido de la biblioteca por parte del intérprete llamado Namedde 48. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
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
</dt> <dt>

[**IWMPPlaylistCollection.getAll (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





