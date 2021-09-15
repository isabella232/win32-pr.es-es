---
title: Atributo WM/WMCollectionGroupID
description: El atributo WM/WMCollectionGroupID es un GUID que identifica el grupo que contiene la colección a la que pertenece el elemento.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Atributo WM/WMCollectionGroupID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571057"
---
# <a name="wmwmcollectiongroupid-attribute"></a>Atributo WM/WMCollectionGroupID

El **atributo WM/WMCollectionGroupID** es un GUID que identifica el grupo que contiene la colección a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**WMCollectionGroupID es** un alias para este atributo.

La Windows DEL SDK de formato multimedia para este atributo es g \_ wszWMCollectionGroupID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





