---
title: Atributo WM/WMContentID
description: El atributo WM/WMContentID es un GUID que identifica el contenido del elemento.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- Atributo WM/WMContentID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f31a42a650d382597e2495d80541d667e229dde09a8181605d83cef65e39945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053763"
---
# <a name="wmwmcontentid-attribute"></a>Atributo WM/WMContentID

El **atributo WM/WMContentID** es un GUID que identifica el contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**WMContentID es** un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMContentID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





