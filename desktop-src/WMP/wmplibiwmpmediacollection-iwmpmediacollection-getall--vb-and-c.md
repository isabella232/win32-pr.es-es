---
title: Método getAll de IWMPMediaCollection
description: El método getAll devuelve una interfaz IWMPPlaylist que corresponde a la lista de reproducción que contiene todos los elementos multimedia de la biblioteca.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- Método getAll Reproductor de Windows Media
- Método getAll Reproductor de Windows Media , interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Reproductor de Windows Media , método getAll
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172710"
---
# <a name="iwmpmediacollectiongetall-method"></a>IWMPMediaCollection::getAll (método)

El **método getAll** devuelve una **interfaz IWMPPlaylist** que corresponde a la lista de reproducción que contiene todos los elementos multimedia de la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción que contiene todos los elementos multimedia solicitados.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del **método getAll** depende de cuál de esas dos maneras se use. Si recupera la interfaz mediante una llamada [a AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el **método getAll** devuelve todos los elementos multimedia de la biblioteca. Sin embargo, si recupera la interfaz mediante una llamada a [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el **método getAll** devuelve solo los elementos de audio de la biblioteca.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa getAll para** reproducir elementos multimedia aleatoriamente desde la colección de medios. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
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
</dt> </dl>

 

 





