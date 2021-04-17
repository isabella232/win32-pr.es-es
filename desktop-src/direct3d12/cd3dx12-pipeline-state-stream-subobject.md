---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT estructura (D3dx12. h)
description: Estructura de aplicación auxiliar con plantilla utilizada para encapsular los pares de datos de tipo de subobjeto y subobjeto como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718502"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>\_Estructura de \_ \_ subobjeto de flujo de estado de canalización CD3DX12 \_

Estructura de aplicación auxiliar con plantilla utilizada para encapsular los pares de datos de tipo de subobjeto y subobjeto como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**
</dt> <dd>

Crea una nueva instancia no inicializada de un subobjeto de \_ flujo de estado de la canalización CD3DX12 \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ Subobjeto de flujo de estado de CANALización \_ \_ \_ (** InnerStructType * * const &i) * *
</dt> <dd>

Crea una nueva \_ \_ \_ \_ instancia de plantilla de subobjeto de flujo de estado de canalización CD3DX12, inicializada con un tipo de subobjeto de [**\_ \_ \_ \_ tipo de subobjeto de estado de canalización D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) y datos de subobjeto copiados de *i*. Tanto el tipo de subobjeto como el tipo de datos del subobjeto se proporcionan como parámetros de plantilla, **Type** y **InnerStructType**, respectivamente. Para obtener más información, vea la sección Comentarios a continuación.

</dd> <dt>

**Operator = (** InnerStructType * * const& i) * *
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador **InnerStructType**() Const**
</dt> <dd>

Conversión implícita al tipo de datos de subobjeto proporcionado por el parámetro de plantilla **InnerStructType** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ El subobjeto de flujo de estado de canalización CD3DX12 \_ es una plantilla definida como sigue:


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



El parámetro de plantilla **InnerStructType** especifica el tipo de datos del subobjeto; es decir, los detalles del subobjeto que se van a codificar en un flujo. El **tipo** de parámetro de plantilla especifica el tipo de subobjeto; es decir, el tipo de la estructura especificada por el parámetro de plantilla **InnerStructType**. El parámetro de plantilla **defaultarg (** especifica un valor opcional en el que se inicializarán los datos del subobjeto cuando una instancia de la creación de instancias de plantilla correspondiente esté construida de forma predeterminada; por ejemplo, para construir el valor predeterminado de una [**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) inicializada con los valores predeterminados de estado de combinación comunes mediante [**CD3DX12 \_ predeterminado**](cd3dx12-default.md).

Estas son las instancias de plantilla definidas:

-   [**\_Marcas de \_ flujo de estado de CANALización CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**CD3DX12 \_ \_ máscara de \_ nodo de flujo de estado de \_ canalización \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**\_ \_ \_ \_ Firma raíz de la secuencia de estado de canalización CD3DX12 \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**\_Diseño de \_ \_ entrada de flujo de estado de canalización CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**Flujo de estado de canalización de CD3DX12 de \_ Estado de canalización \_ \_ \_ IB \_ \_ \_**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**\_ \_ \_ Topología primitiva de flujo de estado \_ de canalización de CD3DX12 \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ frente a**](cd3dx12-pipeline-state-stream-vs.md)
-   [**\_Flujo de estado de canalización \_ \_ \_ GS de CD3DX12**](cd3dx12-pipeline-state-stream-gs.md)
-   [**\_Salida de \_ \_ flujo de flujo de estado de canalización CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**Secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ hs**](cd3dx12-pipeline-state-stream-hs.md)
-   [**\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**\_Flujo de estado de canalización CD3DX12 \_ \_ \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**\_Galería de \_ \_ símbolos de profundidad de flujo de estado de \_ canalización CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**\_Profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**\_Formato de \_ \_ estarcido de profundidad de flujo de estado de \_ \_ canalización CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**\_ \_ \_ Rasterizador de flujo de estado de CANALización de CD3DX12 \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**\_Formatos de \_ \_ destino de representación de secuencia de estado de \_ \_ canalización CD3DX12 \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**\_Ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**\_Máscara de \_ \_ ejemplo de flujo de estado de canalización CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ en caché \_ PSO**](cd3dx12-pipeline-state-stream-cached-pso.md)

Las estructuras de flujo de estado de canalización de CD3DX12 de la secuencia de estado de canalización de CD3DX12, la de profundidad de flujo de estado de canalización de CD3DX12 y de canalización de flujo se definen para inicializar sus datos de subobjeto con valores predeterminados comunes mediante el [**\_ valor predeterminado de CD3DX12**](cd3dx12-default.md). [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-blend-desc.md) [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md) [**\_ \_ \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

