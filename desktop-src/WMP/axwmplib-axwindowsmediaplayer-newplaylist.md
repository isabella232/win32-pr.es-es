---
title: AxWindowsMediaPlayer. reproducción, método
description: El método reproducción devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- método reproducción de Windows Media Player
- método reproducción de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método reproducción
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
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699903"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>AxWindowsMediaPlayer. reproducción, método

El método reproducción devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.

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

**System. String** que es el nombre de la nueva lista de reproducción.

</dd> <dt>

*bstrURL* 
</dt> <dd>

**System. String** que es la dirección URL de la lista de reproducción del metarchivo de Windows Media que se usa para inicializar la nueva lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz WMPLib. IWMPPlaylist que representa la lista de reproducción recién creada.

## <a name="remarks"></a>Observaciones

Si el parámetro *bstrURL* es una cadena null o de longitud cero (""), este método crea una **lista de reproducción** vacía. Si el parámetro *bstrName* es una cadena de longitud cero (""), este método aplica el nombre del metarchivo actual.

La nueva lista de reproducción creada con este método no se agrega a la biblioteca. Para agregar una nueva lista de reproducción a la biblioteca, use IWMPPlaylistCollection. **importPlaylist** o IWMPPlaylistCollection. **reproducción**. Los espacios iniciales o finales del nombre de la lista de reproducción se quitan automáticamente cuando se agregan a la biblioteca.

Dado que la biblioteca permite varias listas de reproducción con el mismo nombre, es posible que desee comprobar la presencia de una lista de reproducción con un nombre determinado antes de agregar una nueva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. reproducción (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





