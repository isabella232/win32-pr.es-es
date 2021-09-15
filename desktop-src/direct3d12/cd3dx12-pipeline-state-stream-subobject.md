---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT estructura (D3dx12.h)
description: Estructura auxiliar con plantilla que se usa para encapsular pares de datos de subobjetos y subobjetos como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569981"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>Estructura DE SUBOBJETO CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_

Estructura auxiliar con plantilla que se usa para encapsular pares de datos de subobjetos y subobjetos como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**SUBOBJETO CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un SUBOBJETO CD3DX12 \_ PIPELINE \_ STATE \_ \_ STREAM.

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT(** InnerStructType** const &i)**
</dt> <dd>

Crea una nueva instancia de plantilla CD3DX12 PIPELINE STATE STREAM SUBOBJECT, inicializada con un \_ \_ tipo de subobjeto \_ \_ [**D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) y datos de subobjetos copiados de i . Tanto el tipo de subobjeto como el tipo de datos de subobjeto se dan como parámetros de plantilla, **Type** e **InnerStructType,** respectivamente. Para obtener más información, vea Comentarios a continuación.

</dd> <dt>

**operator=(** InnerStructType** const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operator **InnerStructType**() const**
</dt> <dd>

Conversión implícita al tipo de datos de subobjeto especificado por el **parámetro de plantilla InnerStructType.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT es una plantilla definida de la siguiente manera:


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



El parámetro de plantilla **InnerStructType** especifica el tipo de datos del subobjeto; es decir, los detalles del subobjeto que se codificarán en una secuencia. El parámetro de **plantilla Type** especifica el tipo de subobjeto; es decir, el tipo de la estructura especificada por el parámetro de plantilla **InnerStructType.** El parámetro de plantilla **DefaultArg** especifica un valor opcional en el que se inicializarán los datos del subobjeto cuando se crea de forma predeterminada una instancia de la creación de instancias de plantilla correspondiente; por ejemplo, para construir de forma predeterminada un DESC DE STREAM [**\_ \_ \_ \_ \_ DESC DE PIPELINE STATE STREAM de CD3DX12**](cd3dx12-pipeline-state-stream-blend-desc.md) inicializado con valores predeterminados comunes de estado de mezcla [**mediante CD3DX12 \_ DEFAULT**](cd3dx12-default.md).

Estas son las instancias de plantilla que se definen:

-   [**MARCAS DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**MÁSCARA DE NODO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**FIRMA RAÍZ DE LA SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**DISEÑO DE ENTRADA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**TOPOLOGÍA PRIMITIVA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ VS**](cd3dx12-pipeline-state-stream-vs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**SALIDA DE FLUJO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE FLUJO DE \_ \_ ESTADO DE \_ CANALIZACIÓN \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**FORMATO DE GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE FLUJO DE ESTADO DE \_ \_ CANALIZACIÓN \_ \_ \_ CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**RASTERIZADOR DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**FORMATOS DE DESTINO DE REPRESENTACIÓN DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**EJEMPLO \_ \_ \_ \_ DESC DESC DE SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12 \_**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**MÁSCARA DE EJEMPLO DE SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CACHED \_ PSO**](cd3dx12-pipeline-state-stream-cached-pso.md)

Las estructuras [**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL,**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)y [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) se definen para inicializar sus datos de subobjeto con valores predeterminados comunes mediante [**CD3DX12 \_ DEFAULT.**](cd3dx12-default.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**TIPO DE SUBOBJETO DE ESTADO \_ \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

