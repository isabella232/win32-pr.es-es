---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de \_ DESC de la firma raíz de D3D12 \_ \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Estructura de CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717590"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>CD3DX12 \_ estructura de \_ \_ DESC de firma raíz con versión \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de DESC de la [**\_ \_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 de \_ firma raíz con control de versiones \_ \_ \_ ()**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una descripción de la \_ firma raíz con versión CD3DX12 \_ \_ \_ .

</dd> <dt>

**CD3DX12 de \_ firma raíz de versión explícita de la \_ firma de raíz \_ \_ (const D3D12 con \_ versión de \_ firma raíz con \_ \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de la \_ firma raíz con versión CD3DX12 \_ \_ , inicializada con el contenido de una estructura de DESC de la [**\_ \_ \_ firma \_ raíz con versión D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

</dd> <dt>

**Descripción de la firma raíz de CD3DX12 explícita con \_ versión \_ \_ \_ (const D3D12 raíz de la \_ \_ &firma raíz \_ )**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de la \_ firma raíz con versión CD3DX12 \_ \_ , inicializada con el contenido de una estructura de DESC de la [**\_ \_ firma \_ raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 de \_ firma raíz explícita con versión de \_ \_ \_ (const D3D12 \_ raíz \_ signatura \_ DESC1 &)**
</dt> <dd>

Crea una nueva instancia de una CD3DX12 de \_ \_ firma raíz con control de versiones \_ \_ , inicializada con el contenido de una estructura DESC1 de la [**\_ \_ firma \_ raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .

</dd> <dt>

**CD3DX12 \_ \_ de firma raíz con control \_ de versiones \_ (uint numParameters, const D3D12 \_ raíz \_ parámetro \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de \_ firma raíz \_ \_ None)**
</dt> <dd>

Crea una nueva instancia de una \_ \_ Descripción de la firma raíz CD3DX12 con versión \_ \_ , inicializando los siguientes parámetros:

UINT numParameters

[**\_ \_ parámetro raíz const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ \_ de firma raíz con control \_ de versiones \_ (uint numParameters, const D3D12 \_ raíz \_ parámetro1 \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de \_ firma raíz \_ \_ None)**
</dt> <dd>

Crea una nueva instancia de una \_ \_ Descripción de la firma raíz CD3DX12 con versión \_ \_ , inicializando los siguientes parámetros:

UINT numParameters

const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**CD3DX12 de \_ firma raíz con versiones de \_ \_ \_ ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de una \_ \_ Descripción de la firma raíz con versión CD3DX12 \_ \_ , inicializada con los parámetros predeterminados:

UINT numParameters = 0

const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = null

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**Inicialización en línea \_ 1 \_ 0 (uint numParameters, const D3D12 \_ raíz \_ parámetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 marca de \_ firma raíz \_ \_ \_ None)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numParameters

[**\_ \_ parámetro raíz const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**Static inline init \_ 1 \_ 0 (D3D12 con \_ versiones \_ \_ de la firma raíz \_ DESC &DESC, uint numParameters, const D3D12 \_ raíz \_ parámetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de firma raíz \_ \_ \_ None)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Descripción de \_ la \_ firma \_ raíz con versión**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

UINT numParameters

[**\_ \_ parámetro raíz const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**Inicialización en línea \_ 1 \_ (uint numParameters, const D3D12 \_ raíz \_ Parámetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de firma raíz \_ \_ \_ None)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numParameters

const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**Inicial de inline init \_ 1 \_ 1 (D3D12 de \_ firma raíz con versiones de \_ \_ \_ &DESC, uint numParameters, const D3D12 \_ raíz \_ parámetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de \_ firma raíz \_ \_ None)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Descripción de \_ la \_ firma \_ raíz con versión**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

UINT numParameters

const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Descripción de la \_ \_ firma raíz \_ de D3D12 con versiones**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





