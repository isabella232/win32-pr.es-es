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
ms.openlocfilehash: 0f35ca1964df5b99658c868bbc46f04ef67e6c9be821d6849be279de20ffaf9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900295"
---
# <a name="wmwmcollectiongroupid-attribute"></a>Atributo WM/WMCollectionGroupID

El **atributo WM/WMCollectionGroupID** es un GUID que identifica el grupo que contiene la colección a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**WMCollectionGroupID es** un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMCollectionGroupID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





