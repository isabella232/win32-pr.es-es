---
title: MediaCollection. Add (método)
description: El método Add agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca. | MediaCollection. Add (método)
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Agregar método Media Player de Windows
- Agregar método Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, Add (método)
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
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690642"
---
# <a name="mediacollectionadd-method"></a>MediaCollection. Add (método)

El método **Add** agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ruta de acceso* \[ de\]
</dt> <dd>

**Cadena** que contiene la ruta de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **multimedia** .

## <a name="remarks"></a>Observaciones

Este método carga un elemento multimedia o una lista de reproducción existente en la biblioteca, dada una ruta de acceso a un archivo. Este método no mueve ni cambia el archivo. Este método produce un error si se proporciona una ruta de acceso local no válida, pero no se comprueba la validez de los archivos multimedia digitales antes de que se agreguen a la biblioteca.

Este método acepta archivos de lista de reproducción estática y automática. *PlaylistCollection*. el método **importPlaylist** también se puede usar para agregar una lista de reproducción estática a la biblioteca.

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de Microsoft JScript se agregan tres objetos multimedia a la colección de medios de Windows Media Player. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection. Remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





