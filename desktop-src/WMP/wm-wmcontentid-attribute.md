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
ms.openlocfilehash: 04366991a37b727f2693bc42ce2050139ce5c211
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359862"
---
# <a name="wmwmcontentid-attribute"></a>Atributo WM/WMContentID

El **atributo WM/WMContentID** es un GUID que identifica el contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**WMContentID es** un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMContentID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





