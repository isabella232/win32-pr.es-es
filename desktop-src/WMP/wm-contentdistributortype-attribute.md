---
title: Atributo WM/ContentDistributorType
description: El atributo WM/ContentDistributorType es el tipo del distribuidor del elemento.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Atributo WM/ContentDistributorType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466417"
---
# <a name="wmcontentdistributortype-attribute"></a>Atributo WM/ContentDistributorType

El **atributo WM/ContentDistributorType** es el tipo del distribuidor del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

El valor de este atributo se establecerá en "List" o "Radio". Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**ContentDistributorType es** un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMContentDistributorType.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





