---
title: ErrorItem. Condition
description: La propiedad Condition recupera un valor que indica la condición del error.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. Condition Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700106"
---
# <a name="erroritemcondition"></a>ErrorItem. Condition

La propiedad **Condition** recupera un valor que indica la condición del error.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**) que representa el código de condición.

## <a name="remarks"></a>Observaciones

El código de condición es un valor que usa Microsoft para proporcionar información adicional al personal de soporte técnico.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





