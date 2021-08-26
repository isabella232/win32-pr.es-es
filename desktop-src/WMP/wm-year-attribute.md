---
title: Atributo WM/Year
description: El atributo WM/Year es el año en que se publicó el contenido.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Atributo WM/Year Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0b76fbf54a53a7ae09728fe34d75fff5c232de9ecfa13a77edaa97cd37e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900195"
---
# <a name="wmyear-attribute"></a>Atributo WM/Year

El **atributo WM/Year** es el año en que se publicó el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo solo se almacena en el archivo multimedia digital.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

Este atributo no debe usarse como parte de una condición de consulta. Se deriva de otro atributo y no se puede consultar directamente en una colección de medios.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMYear.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 Reproductor de Windows Media 10 o posterior no admite este atributo<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





