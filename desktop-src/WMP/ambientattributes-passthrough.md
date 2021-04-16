---
title: AmbientAttributes. passThrough
description: El atributo passThrough especifica o recupera un valor que indica si el control pasará todos los eventos del mouse por el control situado bajo él.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- AmbientAttributes. passThrough Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699430"
---
# <a name="ambientattributespassthrough"></a>AmbientAttributes. passThrough

El atributo **passThrough** especifica o recupera un valor que indica si el control pasará todos los eventos del mouse por el control situado bajo él.

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | El control pasa los eventos a través del control. |
| false | Predeterminada. El control no pasa los eventos a través de.         |



 

## <a name="remarks"></a>Observaciones

Este atributo es útil si, por ejemplo, un control de texto se coloca sobre un control de botón solo para proporcionar etiquetas. En este caso, los clics en el control de texto se deben pasar al control de botón.

Los elementos de **vista**, **subvista** y **lista de reproducción** no admiten el atributo **passThrough** . No funcionará con el elemento de **vídeo** si se trata de un *vídeo*. **Windowless** está establecido en false, y en el elemento **Effects** si tiene *efectos*. **windowed** está establecido en true.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





