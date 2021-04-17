---
title: ErrorItem.errorContext
description: La propiedad errorContext recupera un valor que indica el contexto del error.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorContext Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698629"
---
# <a name="erroritemerrorcontext"></a>ErrorItem.errorContext

La propiedad **errorContext** recupera un valor que indica el contexto del error.

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura que representa el código de contexto del error.

## <a name="remarks"></a>Observaciones

El contexto de error es información que Microsoft usa para proporcionar información adicional para el personal de soporte técnico.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve una cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/>                               |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





