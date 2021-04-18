---
title: EFFECTs. fullScreen
description: El atributo fullScreen especifica o recupera un valor que indica si la visualización actual se muestra en pantalla completa. Este atributo solo se puede establecer en tiempo de ejecución.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFECTs. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700241"
---
# <a name="effectsfullscreen"></a>EFFECTs. fullScreen

El atributo **Fullscreen** especifica o recupera un valor que indica si la visualización actual se muestra en pantalla completa. Este atributo solo se puede establecer en tiempo de ejecución.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                          |
|-------|------------------------------------------------------|
| true  | La visualización se muestra en pantalla completa.              |
| false | Predeterminada. La visualización no se muestra en pantalla completa. |



 

## <a name="remarks"></a>Observaciones

Una visualización solo se puede poner en modo de pantalla completa mientras el contenido multimedia se reproduce o está en pausa. Si es *Player*. **currentMedia** es un vídeo, un complemento de vídeo debe estar presente. Si es audio, debe existir un complemento de visualización que admita la presentación en pantalla completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> </dl>

 

 





