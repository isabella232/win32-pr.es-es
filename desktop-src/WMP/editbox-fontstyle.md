---
title: EDITBOX.fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control de cuadro de edición.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EDITBOX.fontStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241064"
---
# <a name="editboxfontstyle"></a>EDITBOX.fontStyle

El **atributo fontStyle** especifica o recupera el estilo de fuente para el control de cuadro de edición.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno o varios de los valores siguientes.



| Value     | Descripción           |
|-----------|-----------------------|
| Negrita      | Estilo de fuente en negrita.      |
| Cursiva    | Estilo de fuente cursiva.    |
| Subrayado | Estilo de fuente de subrayado. |
| Tachado | Estilo de fuente de tachón. |
| Normal    | Estilo de fuente normal.    |



 

## <a name="remarks"></a>Observaciones

Se puede usar cualquier combinación de los valores, separados por espacios. El estilo Normal tiene prioridad sobre todos los demás valores y se omitirán los demás especificados junto con Normal.

Con fines de representación, Normal es el estilo de fuente predeterminado. El valor predeterminado recuperado de este atributo es "" (cadena vacía).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontFace**](editbox-fontface.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





