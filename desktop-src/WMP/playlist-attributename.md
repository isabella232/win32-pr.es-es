---
title: Playlist.attributeName
description: La propiedad attributeName recupera el nombre de un atributo en un índice especificado.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Playlist.attributeName Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359533"
---
# <a name="playlistattributename"></a>Playlist.attributeName

La **propiedad attributeName** recupera el nombre de un atributo en un índice especificado.

## <a name="syntax"></a>Sintaxis

*player*. *currentPlaylist*. **attributeName**( *index* )

## <a name="parameters"></a>Parámetros

*índice*

**Number** (**long**) que contiene el índice.

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

La propiedad **attributeCount** recupera el número de atributos. Dado un índice, **attributeName** devuelve una **cadena** que se puede usar junto con **setItemInfo** u **getItemInfo** para especificar o recuperar un valor para el atributo.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

Vea la [propiedad attributeCount](playlist-attributecount.md) para obtener código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





