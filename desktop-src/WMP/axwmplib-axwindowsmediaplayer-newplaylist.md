---
title: Método AxWindowsMediaPlayer.newPlaylist
description: El método newPlaylist devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- Método newPlaylist Reproductor de Windows Media
- Método newPlaylist Reproductor de Windows Media , clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , método newPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35bbc1d1c8a0f1f76d685676e08119b659ad119176036ab377f9525ce1ab0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123895"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>Método AxWindowsMediaPlayer.newPlaylist

El método newPlaylist devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* 
</dt> <dd>

**System.String que** es el nombre de la nueva lista de reproducción.

</dd> <dt>

*bstrURL* 
</dt> <dd>

**System.String que es** la dirección URL de la lista de Windows de metarchivo multimedia que se usa para inicializar la nueva lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz WMPLib.IWMPPlaylist que representa la lista de reproducción recién creada.

## <a name="remarks"></a>Comentarios

Si el *parámetro bstrURL* es una cadena de longitud nula o cero (""), este método crea una lista de **reproducción vacía.** Si el *parámetro bstrName* es una cadena de longitud cero (""), este método aplica el nombre del metarchivo actual.

La nueva lista de reproducción creada con este método no se agrega a la biblioteca. Para agregar una nueva lista de reproducción a la biblioteca, use IWMPPlaylistCollection. **importPlaylist** o IWMPPlaylistCollection. **newPlaylist**. Los espacios iniciales o finales del nombre de la lista de reproducción se quitan automáticamente cuando se agrega a la biblioteca.

Dado que la biblioteca permite varias listas de reproducción con el mismo nombre, es posible que quiera comprobar la presencia de una lista de reproducción con un nombre determinado antes de agregar una nueva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.importPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





