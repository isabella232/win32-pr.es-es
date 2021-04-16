---
title: Lista de reproducción. attributeName
description: La propiedad attributeName recupera el nombre de un atributo en un índice especificado.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Lista de Media Player de Windows. attributeName
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708869"
---
# <a name="playlistattributename"></a>Lista de reproducción. attributeName

La propiedad **attributeName** recupera el nombre de un atributo en un índice especificado.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentPlaylist*. **attributeName**( *Índice* )

## <a name="parameters"></a>Parámetros

*índice*

**Número** (**largo**) que contiene el índice.

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

La propiedad **attributeCount** recupera el número de atributos. Dado un índice, **attributeName** devuelve una **cadena** que se puede usar junto con **setItemInfo** o **getItemInfo** para especificar o recuperar un valor para el atributo.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

Vea la propiedad [attributeCount](playlist-attributecount.md) para ver el código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Lista de reproducción. attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Lista de reproducción. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Lista de reproducción. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





