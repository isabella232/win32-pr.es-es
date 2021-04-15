---
title: Atributo WM/WMContentID
description: El atributo WM/WMContentID es un GUID que identifica el contenido del elemento.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- Media Player de Windows de atributos de WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04366991a37b727f2693bc42ce2050139ce5c211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708989"
---
# <a name="wmwmcontentid-attribute"></a>Atributo WM/WMContentID

El atributo **WM/WMContentID** es un GUID que identifica el contenido del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**WMContentID** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMContentID.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





