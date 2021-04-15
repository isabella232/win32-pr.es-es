---
title: Atributo WM/ContentDistributorType
description: El atributo WM/ContentDistributorType es el tipo del distribuidor del elemento.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Media Player de Windows de atributos de WM/ContentDistributorType
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708730"
---
# <a name="wmcontentdistributortype-attribute"></a>Atributo WM/ContentDistributorType

El atributo **WM/ContentDistributorType** es el tipo del distribuidor del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

El valor de este atributo se establecerá en "list" o "radio". Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

**ContentDistributorType** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMContentDistributorType.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





