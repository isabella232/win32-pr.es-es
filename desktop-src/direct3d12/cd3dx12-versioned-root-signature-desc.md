---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ \_ \_ DESC DESC de firma raíz con control de versiones \_ D3D12.
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965020"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>ESTRUCTURA \_ \_ \_ \_ DESC DESC DE FIRMA RAÍZ CON VERSIONES DE CD3DX12

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ \_ \_ \_ DESC DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) de firma raíz con control de versiones D3D12.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ DESC DESC DE FIRMA RAÍZ CON VERSIÓN \_ \_ \_ CD3DX12.

</dd> <dt>

**EXPLICIT CD3DX12 \_ \_ VERSIONED ROOT \_ SIGNATURE \_ DESC(const D3D12 \_ \_ VERSIONED ROOT SIGNATURE \_ \_ DESC &o)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC DE FIRMA RAÍZ CON CONTROL DE VERSIONES DE CD3DX12, inicializado con el contenido de una estructura \_ \_ \_ \_ [**\_ \_ \_ \_ DESC DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) de firma raíz con control de versiones D3D12.

</dd> <dt>

**EXPLICIT CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC &o)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC DE FIRMA RAÍZ CON CONTROL DE VERSIONES DE CD3DX12, inicializado con el contenido de una estructura DESC de firma raíz \_ \_ \_ \_ [**D3D12. \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)

</dd> <dt>

**EXPLICIT CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC1 &o)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC DE FIRMA RAÍZ VERSIONED DESC de CD3DX12, inicializado con el contenido de una estructura \_ \_ \_ \_ [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de UN DESC DESC DE FIRMA RAÍZ CON CONTROL DE VERSIONES DE CD3DX12, \_ \_ \_ \_ inicializando los parámetros siguientes:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de UN DESC DESC DE FIRMA RAÍZ CON CONTROL DE VERSIONES DE CD3DX12, \_ \_ \_ \_ inicializando los parámetros siguientes:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC DE FIRMA RAÍZ VERSIONED DESC de CD3DX12, \_ \_ \_ \_ inicializado con los parámetros predeterminados:

UINT numParameters = 0

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = NULL

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**inline Init \_ 1 \_ 0(UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**static inline Init \_ 1 \_ 0(D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 STATIC \_ \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**inline Init \_ 1 \_ 1(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> <dt>

**static inline Init \_ 1 \_ 1(D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ MARCAS \_ DE FIRMA RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





