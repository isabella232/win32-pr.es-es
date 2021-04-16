---
title: Atributo WM/UniqueFileIdentifier
description: El atributo WM/UniqueFileIdentifier es una cadena que identifica de forma única el elemento.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Media Player de Windows de atributos de WM/UniqueFileIdentifier
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a4297f299f6e7df64088066b3137d844a0c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649929"
---
# <a name="wmuniquefileidentifier-attribute"></a>Atributo WM/UniqueFileIdentifier

El atributo **WM/UniqueFileIdentifier** es una cadena que identifica de forma única el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**UniqueFileIdentifier** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMUniqueFileIdentifier.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





