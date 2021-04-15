---
title: Atributo WM/ProtectionType
description: El atributo WM/ProtectionType es el tipo de protección que se usa en el contenido.
ms.assetid: aab36b57-5b4e-4a3f-80cf-872ec8369c49
keywords:
- Media Player de Windows de atributos de WM/ProtectionType
topic_type:
- apiref
api_name:
- WM/ProtectionType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf2b9c4700cb45ca5daf2c7d9290456beefbf1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709021"
---
# <a name="wmprotectiontype-attribute"></a>Atributo WM/ProtectionType

El atributo **WM/ProtectionType** es el tipo de protección que se usa en el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

**ProtectionType** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProtectionType.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





