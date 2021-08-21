---
title: CD3DX12_DEFAULT estructura (D3dx12.h)
description: Pasa D3D12 \_ DEFAULT a un constructor para cada estructura auxiliar. Esta estructura se usa simplemente como mecanismo para establecer parámetros predeterminados en las otras estructuras auxiliares.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT estructura
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
ms.openlocfilehash: 876fbb5e666680e85854196fb9136bfd4d765d6eecf8f16bf6101bb321a7039a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531292"
---
# <a name="cd3dx12_default-structure"></a>CD3DX12 \_ DEFAULT (estructura)

Pasa D3D12 \_ DEFAULT a un constructor para cada estructura auxiliar. Esta estructura se usa simplemente como mecanismo para establecer parámetros predeterminados en las otras estructuras auxiliares.

## <a name="remarks"></a>Comentarios

Esta estructura se declara de la siguiente manera:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Pasa D3D12 \_ DEFAULT a un constructor para cada estructura auxiliar. Por ejemplo, el constructor siguiente se declara en d3dx12.h:

IDENTIFICADOR DEL \_ DESCRIPTOR DE CPU CD3DX12(CD3DX12 \_ \_ \_ DEFAULT) { ptr = 0; }

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





