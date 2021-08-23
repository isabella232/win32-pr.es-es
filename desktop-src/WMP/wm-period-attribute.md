---
title: Atributo WM/Period
description: El atributo WM/Period es el período del contenido.
ms.assetid: fb154ef7-c8bc-4468-8f3f-4b716291fd0a
keywords:
- Atributo WM/Period Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Period
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a46be5c66fb2dc6f9f6739a57778deef04b113f174208c5d56fe0712589aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053813"
---
# <a name="wmperiod-attribute"></a>Atributo WM/Period

El **atributo WM/Period** es el período del contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**Period** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMPeriod.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





