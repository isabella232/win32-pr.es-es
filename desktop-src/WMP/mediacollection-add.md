---
title: Método MediaCollection.add
description: El método add agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca. | Método MediaCollection.add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- add method Reproductor de Windows Media
- add method Reproductor de Windows Media , Clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media , agregar método
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b26d21f67496f345324efdca93dbf85e59947f1616e0c5620faead2807a6ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647915"
---
# <a name="mediacollectionadd-method"></a>Método MediaCollection.add

El **método add** agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ruta de acceso* \[ En\]
</dt> <dd>

**Cadena** que contiene la ruta de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto Media.**

## <a name="remarks"></a>Comentarios

Este método carga un elemento multimedia o una lista de reproducción existentes en la biblioteca, dada una ruta de acceso a un archivo. Este método no mueve ni cambia el archivo. Este método produce un error si se le da una ruta de acceso local no válida, pero no se comprueba la validez de los archivos multimedia digitales antes de agregarse a la biblioteca.

Este método acepta archivos de lista de reproducción estáticos y automáticos. *PlaylistCollection*. **El método importPlaylist** también se puede usar para agregar una lista de reproducción estática a la biblioteca.

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo JScript microsoft agrega tres objetos multimedia a la colección Reproductor de Windows Media multimedia. El **objeto Player** se creó con ID="Player".


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





