---
title: CD3DX12_ROOT_SIGNATURE_DESC estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ \_ DESC de firma raíz D3D12. \_
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- CD3DX12_ROOT_SIGNATURE_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb68acfbe76c4a32e0549da97fbe9dc3c8daae23fe72fc4757f3b840421da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988395"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>Estructura \_ DESC de FIRMA \_ RAÍZ CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ \_ \_ DESC de firma raíz D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ DESC DESC DE FIRMA \_ RAÍZ \_ CD3DX12.

</dd> <dt>

**EXPLICIT CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC &o)**
</dt> <dd>

Crea una nueva instancia de UNA FIRMA RAÍZ DESC CD3DX12, inicializada con el contenido de otra estructura DESC de FIRMA \_ \_ RAÍZ \_ [**\_ \_ D3D12. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)

</dd> <dt>

**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC DESC DE FIRMA RAÍZ \_ CD3DX12, \_ inicializando los parámetros siguientes:

UINT numParameters

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

(opt) UINT numStaticSamplers = 0

(opt) [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

(opt) [**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ ROOT \_ SIGNATURE \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC DESC DE FIRMA RAÍZ \_ CD3DX12, \_ inicializado con parámetros predeterminados.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**inline Init(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numParameters

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

(opt) UINT numStaticSamplers = 0

(opt) [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

(opt) [**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**static inline Init(D3D12 \_ ROOT \_ SIGNATURE \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 STATIC \_ \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc

UINT numParameters

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

(opt) UINT numStaticSamplers = 0

(opt) [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

(opt) [**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





