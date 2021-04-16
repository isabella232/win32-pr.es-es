---
title: CD3DX12_DEFAULT estructura (D3dx12. h)
description: Pasa \_ el valor predeterminado de D3D12 en un constructor para cada estructura de aplicación auxiliar. Esta estructura simplemente se usa como mecanismo para establecer los parámetros predeterminados en las otras estructuras auxiliares.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Estructura de CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649387"
---
# <a name="cd3dx12_default-structure"></a>\_Estructura predeterminada de CD3DX12

Pasa \_ el valor predeterminado de D3D12 en un constructor para cada estructura de aplicación auxiliar. Esta estructura simplemente se usa como mecanismo para establecer los parámetros predeterminados en las otras estructuras auxiliares.

## <a name="remarks"></a>Observaciones

Este struct se declara de la siguiente manera:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Pasa \_ el valor predeterminado de D3D12 en un constructor para cada struct de la aplicación auxiliar. Por ejemplo, el siguiente constructor se declara en d3dx12. h:

\_Identificador de \_ descriptor de CPU de CD3DX12 \_ ( \_ valor predeterminado de CD3DX12) {PTR = 0;}

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





