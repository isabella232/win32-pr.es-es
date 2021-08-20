---
title: ErrorItem.condition
description: La propiedad condition recupera un valor que indica la condición del error.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem.condition Reproductor de Windows Media
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
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996645"
---
# <a name="erroritemcondition"></a>ErrorItem.condition

La **propiedad** condition recupera un valor que indica la condición del error.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un number **(long)** de solo lectura que representa el código de condición.

## <a name="remarks"></a>Comentarios

El código de condición es un valor que microsoft usa para proporcionar información adicional al personal de soporte técnico.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





