---
description: Esta macro crea un valor que usa el problema para emitir un final de la consulta.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362616"
---
# <a name="d3dissue_end"></a>Final de D3DISSUE \_

Esta macro crea un valor que usa el [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) para emitir un final de la consulta.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Parámetros





 

## <a name="remarks"></a>Observaciones

Esta macro cambia el estado de la consulta a no señalado.

D3DISSUE \_ End es válido para los siguientes tipos de consulta.

-   D3DQUERYTYPE \_ VCACHE
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ VERTEXSTATS
-   \_Evento D3DQUERYTYPE
-   Oclusión de D3DQUERYTYPE \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**Inicio de D3DISSUE \_**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
