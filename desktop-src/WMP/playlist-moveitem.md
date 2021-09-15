---
title: Método Playlist.moveItem
description: El método moveItem cambia la ubicación de un elemento en la lista de reproducción.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Método moveItem Reproductor de Windows Media
- Método moveItem Reproductor de Windows Media , clase Playlist
- Clase playlist Reproductor de Windows Media método , moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466156"
---
# <a name="playlistmoveitem-method"></a>Método Playlist.moveItem

El **método moveItem** cambia la ubicación de un elemento en la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*oldIndex* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice antiguo.

</dd> <dt>

*newIndex* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el nuevo índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las listas de reproducción almacenadas en la biblioteca pueden cambiar fuera de su control. Asegúrese de supervisar y controlar todos los eventos relacionados con la lista de reproducción adecuados para que el orden de los elementos de la lista de reproducción no cambie inesperadamente.

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





