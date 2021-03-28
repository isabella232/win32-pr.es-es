---
title: D3DX11_STATE_BLOCK_MASK estructura (D3dx11effect. h)
description: Indica el estado del dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362671"
---
# <a name="d3dx11_state_block_mask-structure"></a>\_Estructura de \_ máscara de bloque de estado D3DX11 \_

Indica el estado del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>Miembros

<dl> <dt>

**VIRTUAL**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del sombreador de vértices.

</dd> <dt>

**VSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de muestreadores de sombreador de vértices. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.

</dd> <dt>

**VSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos del sombreador de vértices. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de constantes de sombreador de vértices. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.

</dd> <dt>

**VSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces del sombreador de vértices. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.

</dd> <dt>

**!**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del sombreador de casco.

</dd> <dt>

**HSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de muestreadores de sombreador de casco. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.

</dd> <dt>

**HSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos del sombreador de casco. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de constantes de sombreador de casco. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.

</dd> <dt>

**HSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de casco. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.

</dd> <dt>

**DIRECTORIO**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del sombreador de dominio.

</dd> <dt>

**DSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de muestreadores de sombreador de dominio. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.

</dd> <dt>

**DSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos del sombreador de dominio. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de constantes de sombreador de dominio. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer.

</dd> <dt>

**DSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de dominio. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.

</dd> <dt>

**GS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del sombreador de geometría.

</dd> <dt>

**GSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de muestreadores de sombreador de geometría. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.

</dd> <dt>

**GSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos del sombreador de geometría. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de constantes de sombreador de geometría. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer.

</dd> <dt>

**GSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de geometría. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.

</dd> <dt>

**PS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del sombreador de píxeles.

</dd> <dt>

**PSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de muestreadores de sombreador de píxeles. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.

</dd> <dt>

**PSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos del sombreador de píxeles. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de constantes de sombreador de píxeles. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.

</dd> <dt>

**PSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de píxeles. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se van a guardar las vistas de acceso desordenado del sombreador de píxeles.

</dd> <dt>

**CS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del sombreador de cálculo.

</dd> <dt>

**CSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de muestreadores de sombreador de proceso. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.

</dd> <dt>

**CSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos del sombreador de cálculo. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de constantes de sombreador de cálculo. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.

</dd> <dt>

**CSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de cálculo. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se van a guardar las vistas de acceso desordenado del sombreador de cálculo.

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de búferes de vértices. La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del búfer de índice.

</dd> <dt>

**IAInputLayout**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se va a guardar el estado de diseño de entrada.

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se va a guardar el estado de la topología primitiva.

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se deben guardar los Estados de destinos de representación.

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se va a guardar el estado de la galería de símbolos de profundidad.

</dd> <dt>

**OMBlendState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se va a guardar el estado de Blend.

</dd> <dt>

**RSViewports**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se van a guardar los Estados de las ventanillas.

</dd> <dt>

**RSScissorRects**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se deben guardar los Estados de rectángulos en tijera.

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se debe guardar el estado del rasterizador.

</dd> <dt>

**SOBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se van a guardar los Estados de los búferes de flujo de salida.

</dd> <dt>

**Predicación**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booleano que indica si se va a guardar el estado de predication.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una máscara de bloque de estado indica el dispositivo que cambia un paso o una técnica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

