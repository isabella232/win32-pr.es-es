---
title: Atributo de archivo
description: El atributo de archivo es el tamaño del archivo en bytes.
ms.assetid: e845cc82-6975-4fd9-800f-a66f59a5fb39
keywords:
- Archivos de Media Player de Windows de atributos
topic_type:
- apiref
api_name:
- FileSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee243d85be59502acead3614dced49494c11104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699716"
---
# <a name="filesize-attribute"></a>Atributo de archivo

El **atributo de archivo es** el tamaño del archivo en bytes.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotografía](photo-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

**Size** es un alias de este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMFileSize.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior (el elemento de fotografía solo se admite en Windows Media Player 10 o posterior)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





