---
title: Creación de una firma raíz
description: Las firmas raíz son una estructura de datos compleja que contiene estructuras anidadas.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3705f4e1a0a88841560d67d5904e0f1b5dabd3f8
ms.sourcegitcommit: a0cb986d5694b69d4a65b7d42a22694d02a6e83a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108296340"
---
# <a name="creating-a-root-signature"></a>Creación de una firma raíz

Las firmas raíz son una estructura de datos compleja que contiene estructuras anidadas. Se pueden definir mediante programación mediante la definición de estructura de datos siguiente (que incluye métodos para ayudar a inicializar miembros). Como alternativa, se pueden crear en lenguaje de sombreado de alto nivel (HLSL), lo que ofrece la ventaja de que el compilador validará pronto que el diseño es compatible con el sombreador.

La API para crear una firma raíz toma una versión serializada (independiente, sin puntero) de la descripción del diseño que se describe a continuación. Se proporciona un método para generar esta versión serializada a partir de la estructura de datos de C++, pero otra manera de obtener una definición de firma raíz serializada es recuperarla de un sombreador compilado con una firma raíz.

Si desea aprovechar las optimizaciones de controladores para los datos y descriptores de firma raíz, consulte [Root Signature Version 1.1 (Versión de firma raíz 1.1).](root-signature-version-1-1.md)

-   [Tipos de enlace de tabla descriptor](#descriptor-table-bind-types)
-   [Intervalo de descriptor](#descriptor-range)
-   [Diseño de tabla descriptor](#descriptor-table-layout)
-   [Constantes raíz](#root-constants)
-   [Descriptor raíz](#root-descriptor)
-   [Visibilidad del sombreador](#shader-visibility)
-   [Definición de firma raíz](#root-signature-definition)
-   [Serialización y deserialización de la estructura de datos de firma raíz](/windows)
-   [API de creación de firmas raíz](#root-signature-creation-api)
-   [Firma raíz en objetos de estado de canalización](#root-signature-in-pipeline-state-objects)
-   [Código para definir una firma raíz de la versión 1.1](#code-for-defining-a-version-11-root-signature)
-   [Temas relacionados](#related-topics)

## <a name="descriptor-table-bind-types"></a>Tipos de enlace de tabla descriptor

La enumeración [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) define los tipos de descriptores a los que se puede hacer referencia como parte de una definición de diseño de tabla de descriptores.

Es un intervalo para que, por ejemplo, si parte de una tabla de descriptores tiene 100 SRV, ese intervalo se puede declarar en una entrada en lugar de en 100. Por lo tanto, una definición de tabla de descriptores es una colección de intervalos.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Intervalo de descriptores

La [**estructura D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) define un intervalo de descriptores de un tipo determinado (como SRV) dentro de una tabla de descriptores.

La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro se puede usar normalmente para el parámetro de `OffsetInDescriptorsFromTableStart` [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Esto significa anexar el intervalo de descriptor que se define después del anterior en la tabla de descriptores. Si la aplicación quiere usar descriptores de alias o, por algún motivo, quiere omitir ranuras, puede establecer en el `OffsetInDescriptorsFromTableStart` desplazamiento deseado. La definición de intervalos superpuestos de distintos tipos no es válida.

El conjunto de registros de sombreador especificados por la combinación de , , y no puede tener conflictos ni superponerse entre las declaraciones de una firma raíz que tengan Visibilidad común del sombreador `RangeType` `NumDescriptors` `BaseShaderRegister` `RegisterSpace` [**\_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (consulte la sección de visibilidad del sombreador siguiente).

## <a name="descriptor-table-layout"></a>Diseño de tabla de descriptores

La [**estructura D3D12 \_ ROOT DESCRIPTOR \_ \_ TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) declara el diseño de una tabla de descriptores como una colección de intervalos de descriptores que aparecen uno tras otro en un montón de descriptores. No se permiten muestreadores en la misma tabla de descriptores que CBV/UAV/SRV.

Esta estructura se usa cuando el tipo de ranura de firma raíz se establece en `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Para establecer una tabla de descriptores de gráficos (CBV, SRV, UAV, Sampler), use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Para establecer una tabla de descriptores de proceso, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Constantes raíz

La [**estructura D3D12 \_ ROOT \_ CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) declara constantes insertadas en la firma raíz que aparecen en los sombreadores como un búfer constante.

Esta estructura se usa cuando el tipo de ranura de firma raíz se establece en `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Descriptor raíz

La [**estructura D3D12 \_ ROOT \_ DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) declara descriptores (que aparecen en sombreadores) en línea en la firma raíz.

Esta estructura se usa cuando el tipo de ranura de firma raíz se establece en `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` o `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Visibilidad del sombreador

El miembro de la enumeración [**\_ SHADER \_ VISIBILITY de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) establecida en el parámetro de visibilidad del sombreador [**de D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina qué sombreadores ven el contenido de una ranura de firma raíz determinada. El proceso siempre \_ usa ALL (ya que solo hay una fase activa). Los gráficos pueden elegir, pero si usa ALL, todas las fases del \_ sombreador ven lo que está enlazado en la ranura de firma raíz.

Un uso de la visibilidad del sombreador es ayudar con los sombreadores creados que esperan enlaces diferentes por fase de sombreador mediante un espacio de nombres superpuesto. Por ejemplo, un sombreador de vértices puede declarar:

```hlsl
Texture2D foo : register(t0);
```

y el sombreador de píxeles también puede declarar:

```hlsl
Texture2D bar : register(t0);
```

Si la aplicación realiza un enlace de firma raíz a t0 VISIBILITY \_ ALL, ambos sombreadores verán la misma textura. Si el sombreador define realmente quiere que cada sombreador vea texturas diferentes, puede definir 2 ranuras de firma raíz con \_ VISIBILITY VERTEX y \_ PIXEL. Independientemente de la visibilidad que tenga una ranura de firma raíz, siempre tiene el mismo costo (solo en función de lo que sea SlotType) hacia un tamaño de firma raíz máximo fijo.

En el hardware D3D11 de gama baja, SHADER VISIBILITY también se tiene en cuenta al validar los tamaños de las tablas descriptores en un diseño raíz, ya que algún hardware D3D11 solo puede admitir una cantidad máxima de enlaces por \_ fase. Estas restricciones solo se imponen cuando se ejecutan en hardware de bajo nivel y no limitan el hardware más moderno en absoluto.

Si una firma raíz tiene varias tablas descriptoras definidas que se superponen entre sí en el espacio de nombres (los enlaces de registro al sombreador) y cualquiera de ellas especifica ALL para la visibilidad, el diseño no es válido (se producirá un error en la \_ creación).

## <a name="root-signature-definition"></a>Definición de firma raíz

La estructura [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) puede contener tablas de descriptores y constantes insertadas, cada tipo de ranura definido por la estructura ROOT PARAMETER de [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) y la enumeración [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).

Para iniciar una ranura de firma raíz, consulte los métodos **SetComputeRoot \* \* \*** y **\* \* \* SetGraphicsRoot** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

Los muestreadores estáticos se describen en la firma raíz mediante la estructura [**D3D12 \_ STATIC \_ SAMPLER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)

Una serie de marcas limitan el acceso de determinados sombreadores a la firma raíz; consulte [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serialización y deserialización de la estructura de datos de firma raíz

Los métodos descritos en esta sección se exportan mediante D3D12Core.dll y proporcionan métodos para serializar y deserializar una estructura de datos de firma raíz.

El formulario serializado es lo que se pasa a la API al crear una firma raíz. Si se ha creado un sombreador con una firma raíz en él (cuando se agrega esa funcionalidad), el sombreador compilado ya contendrá una firma raíz serializada en él.

Si una aplicación genera por procedimientos una estructura de datos [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) debe crear el formulario serializado mediante [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). Salida de que se puede pasar a [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Si una aplicación ya tiene una firma raíz serializada o tiene un sombreador compilado que contiene una firma raíz y desea detectar mediante programación la definición de diseño (conocida como "reflexión"), se puede llamar a [**D3D12CreateRootSignatureDeserializer.**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) Esto genera una interfaz [**ID3D12RootSignatureDeserializer,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) que contiene un método para devolver la estructura de datos [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserialización. La interfaz posee la duración de la estructura de datos deserialización.

## <a name="root-signature-creation-api"></a>API de creación de firmas raíz

La API [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) toma una versión serializada de una firma raíz.

## <a name="root-signature-in-pipeline-state-objects"></a>Firma raíz en objetos de estado de canalización

Los métodos para crear el estado de canalización ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) toman una interfaz [**OPCIONAL ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) como parámetro de entrada (almacenado en una estructura [**\_ \_ \_ \_ DESC DESC DE ESTADO DE CANALIZACIÓN DE GRÁFICOS D3D12).**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) Esto invalidará cualquier firma raíz que ya se encuentra en los sombreadores.

Si se pasa una firma raíz a uno de los métodos de estado de la canalización de creación, esta firma raíz se valida con todos los sombreadores del PSO por razones de compatibilidad y se le da al controlador que se va a usar con todos los sombreadores. Si alguno de los sombreadores tiene una firma raíz diferente, se reemplaza por la firma raíz que se pasa en la API. Si no se pasa una firma raíz, todos los sombreadores pasados deben tener una firma raíz y deben coincidir; esto se le dará al controlador. Establecer un PSO en una lista o agrupación de comandos no cambia la firma raíz. Esto se logra mediante los [**métodos SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) y [**SetComputeRootSignature.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature) En el momento en que se invoca draw(graphics)/dispatch(compute), la aplicación debe asegurarse de que el PSO actual coincide con la firma raíz actual. de lo contrario, el comportamiento es indefinido.

## <a name="code-for-defining-a-version-11-root-signature"></a>Código para definir una firma raíz de la versión 1.1

En el ejemplo siguiente se muestra cómo crear una firma raíz con el formato siguiente:



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **RootParameterIndex** | **Contents**                                   |                                              |
| \[0\]                  | Constantes raíz: { b2 }                         | (1 CBV)                                      |
| \[1\]                  | Tabla de descriptores: { t2-t7, u0-u3 }             | (6 SRV + 4 UAV)                            |
| \[2\]                  | CBV raíz: { b0 }                               | (1 CBV, datos estáticos)                         |
| \[3\]                  | Tabla de descriptores: { s0-s1 }                    | (2 muestreadores)                                 |
| \[4\]                  | Tabla de descriptores: { t8 - sin enlazar }           | (sin enlazar \# de SRV, descriptores volátiles) |
| \[5\]                  | Tabla de descriptores: { (t0, space1) - unbounded } | (sin enlazar \# de SRV, descriptores volátiles) |
| \[6\]                  | Tabla de descriptores: { b1 }                       | (1 CBV, datos estáticos)                         |



 

Si la mayoría de las partes de la firma raíz se usan la mayoría del tiempo, puede ser mejor que tener que cambiar la firma raíz con demasiada frecuencia. Las aplicaciones deben ordenar las entradas de la firma raíz de cambiar con más frecuencia a menos. Cuando una aplicación cambia los enlaces a cualquier parte de la firma raíz, es posible que el controlador tenga que realizar una copia de parte o de todo el estado de la firma raíz, lo que puede convertirse en un costo notrivial cuando se multiplica entre muchos cambios de estado.

Además, la firma raíz definirá un muestreador estático que realiza el filtrado de textura anisotropica en el registro de sombreador s3.

Una vez enlazada esta firma raíz, se pueden asignar tablas de descriptores, CBV raíz y constantes al \[ espacio de parámetros 0..6. \] Por ejemplo, las tablas de descriptores (intervalos en un montón de descriptores) se pueden enlazar en cada uno de los parámetros raíz 1 y \[ \] \[ 3..6 \] .

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

El código siguiente muestra cómo se podría usar la firma raíz anterior en una lista de comandos gráficos.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Uso de una firma raíz](using-a-root-signature.md)
</dt> </dl>

 

 
