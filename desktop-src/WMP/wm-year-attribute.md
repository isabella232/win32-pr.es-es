---
title: Atributo WM/año
description: El atributo WM/año es el año en que se publicó el contenido.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Atributo de WM/año Media Player de Windows
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653765"
---
# <a name="wmyear-attribute"></a>Atributo WM/año

El atributo **WM/año** es el año en que se publicó el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en el archivo multimedia digital.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

Este atributo no se debe utilizar como parte de una condición de consulta. Se deriva de otro atributo y no se puede consultar directamente en una colección de medios.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMYear.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series Windows Media Player 10 o posterior no admite este atributo<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





