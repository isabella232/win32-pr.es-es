---
title: Atributo WM/ProtectionType
description: El atributo WM/ProtectionType es el tipo de protección que se usa en el contenido.
ms.assetid: aab36b57-5b4e-4a3f-80cf-872ec8369c49
keywords:
- Atributo WM/ProtectionType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/ProtectionType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7888273aaca38a4fb87c5a19fc7c7bc8d47b13a8b6a03a578354b1a8bcd2b3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900355"
---
# <a name="wmprotectiontype-attribute"></a>Atributo WM/ProtectionType

El **atributo WM/ProtectionType** es el tipo de protección que se usa en el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**ProtectionType** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMProtectionType.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





