---
title: CD3DX12_ROOT_SIGNATURE_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de DESC de la firma raíz de D3D12 \_ \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Estructura de CD3DX12_ROOT_SIGNATURE_DESC
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
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718487"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>CD3DX12 \_ \_ \_ estructura DESC de la firma raíz

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de DESC de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

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

**CD3DX12 \_ raíz de la \_ firma raíz \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una descripción de la \_ firma raíz CD3DX12 \_ \_ .

</dd> <dt>

**firma de raíz de CD3DX12 explícita \_ \_ \_ DESC (const D3D12 raíz de la \_ \_ firma raíz \_ &)**
</dt> <dd>

Crea una nueva instancia de una descripción de la \_ firma raíz de CD3DX12 \_ \_ , inicializada con el contenido de otra estructura de DESC de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 \_ root \_ Signature \_ DESC (uint NUMPARAMETERS, const D3D12 \_ raíz \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ PSTATICSAMPLERS = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature Flag \_ \_ None)**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de \_ la firma raíz de CD3DX12 \_ , inicializando los siguientes parámetros:

UINT numParameters

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

rechace UINT numStaticSamplers = 0

rechace [**D3D12 \_ \_Muestra estática \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

rechace [**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ raíz de la \_ firma raíz \_ ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de una descripción de la \_ firma raíz de CD3DX12 \_ \_ , inicializada con los parámetros predeterminados.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**Init en línea (UINT numParameters, const D3D12 \_ raíz \_ parámetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ \_ marca de firma raíz \_ \_ None)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numParameters

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

rechace UINT numStaticSamplers = 0

rechace [**D3D12 \_ \_Muestra estática \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

rechace [**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> <dt>

**Static inline init (D3D12 \_ root \_ SIGNATURE \_ DESC &DESC, uint NUMPARAMETERS, const D3D12 \_ raíz \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ PSTATICSAMPLERS = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ \_ Flag no)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ &de la \_ firma raíz \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)

UINT numParameters

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

rechace UINT numStaticSamplers = 0

rechace [**D3D12 \_ \_Muestra estática \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

rechace [**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Descripción de la \_ firma raíz de D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





