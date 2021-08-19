---
title: Atributo WM/UniqueFileIdentifier
description: El atributo WM/UniqueFileIdentifier es una cadena que identifica de forma única el elemento.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Atributo WM/UniqueFileIdentifier Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf29b5f4a0c2bf6e2642ce13f190a4734a2fb4ff395481b1ba93bc5feeb6db89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930821"
---
# <a name="wmuniquefileidentifier-attribute"></a>Atributo WM/UniqueFileIdentifier

El **atributo WM/UniqueFileIdentifier** es una cadena que identifica de forma única el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**UniqueFileIdentifier** es un alias para este atributo.

La Windows DEL SDK de formato multimedia para este atributo es g \_ wszWMUniqueFileIdentifier.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





