---
title: Crear una firma raíz
description: Las signaturas raíz son una estructura de datos compleja que contiene estructuras anidadas.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2020
ms.locfileid: "104549090"
---
# <a name="creating-a-root-signature"></a>Crear una firma raíz

Las signaturas raíz son una estructura de datos compleja que contiene estructuras anidadas. Se pueden definir mediante programación usando la definición de la estructura de datos siguiente (que incluye métodos para ayudar a inicializar los miembros). Como alternativa, se pueden crear en el lenguaje de sombreado de alto nivel (HLSL), lo que proporciona la ventaja de que el compilador se validará temprano que el diseño es compatible con el sombreador.

La API para crear una firma raíz toma una versión serializada (independiente del puntero) de la descripción del diseño que se describe a continuación. Se proporciona un método para generar esta versión serializada a partir de la estructura de datos de C++, pero otra manera de obtener una definición de la firma raíz serializada es recuperarla de un sombreador que se ha compilado con una firma raíz.

Si desea aprovechar las optimizaciones del controlador para los datos y los descriptores de la firma raíz, consulte la [firma raíz 1,1](root-signature-version-1-1.md)

-   [Tipos de enlace de tabla de descriptores](#descriptor-table-bind-types)
-   [Intervalo de descriptores](#descriptor-range)
-   [Diseño de la tabla de descriptores](#descriptor-table-layout)
-   [Constantes raíz](#root-constants)
-   [Descriptor raíz](#root-descriptor)
-   [Visibilidad del sombreador](#shader-visibility)
-   [Definición de la firma raíz](#root-signature-definition)
-   [Serialización/deserialización de la estructura de datos de la firma raíz](/windows)
-   [API de creación de firma raíz](#root-signature-creation-api)
-   [Firma raíz en objetos de estado de canalización](#root-signature-in-pipeline-state-objects)
-   [Código para definir una firma raíz de la versión 1,1](#code-for-defining-a-version-11-root-signature)
-   [Temas relacionados](#related-topics)

## <a name="descriptor-table-bind-types"></a>Tipos de enlace de tabla de descriptores

El [**tipo de \_ \_ intervalo de \_ descriptor D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) de enumeración define los tipos de descriptores a los que se puede hacer referencia como parte de una definición de diseño de tabla de descriptores.

Es un intervalo para que, por ejemplo, si parte de una tabla de descriptores tiene 100 SRVs, ese intervalo se puede declarar en una entrada en lugar de 100. Por lo tanto, una definición de tabla de descriptores es una colección de intervalos.

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

La estructura de [**\_ \_ intervalo de descriptores de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) define un intervalo de descriptores de un tipo determinado (como SRVs) dentro de una tabla de descriptores.

`D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND`Normalmente, la macro se puede usar para el `OffsetInDescriptorsFromTableStart` parámetro [**de \_ \_ intervalo de descriptor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Esto significa que se anexa el intervalo del descriptor que se define después del anterior en la tabla del descriptor. Si la aplicación desea aplicar un alias a los descriptores o, por algún motivo, quiere omitir las ranuras, puede establecer en el desplazamiento que quiera `OffsetInDescriptorsFromTableStart` . Definir intervalos superpuestos de tipos diferentes no es válido.

El conjunto de registros de sombreador especificado por la combinación de `RangeType` , `NumDescriptors` , `BaseShaderRegister` y `RegisterSpace` no puede entrar en conflicto ni superponerse en las declaraciones de una firma raíz que tengan [**\_ \_ visibilidad del sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) común (consulte la sección de visibilidad del sombreador a continuación).

## <a name="descriptor-table-layout"></a>Diseño de la tabla de descriptores

La estructura de la [**\_ \_ \_ tabla de descriptores raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) declara el diseño de una tabla de descriptores como una colección de intervalos de descriptor que aparecen uno tras otro en un montón de descriptores. No se permiten muestreadores en la misma tabla de descriptores que CBV/UAV/SRVs.

Este struct se utiliza cuando el tipo de ranura de firma raíz está establecido en `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Para establecer una tabla de descriptores de gráficos (CBV, SRV, UAV, muestra), use [**ID3D12GraphicsCommandList:: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Para establecer una tabla de descriptores de proceso, use [**ID3D12GraphicsCommandList:: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Constantes raíz

La estructura de [**\_ \_ constantes raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) declara constantes alineadas en la firma raíz que aparecen en los sombreadores como un búfer de constantes.

Este struct se utiliza cuando el tipo de ranura de firma raíz está establecido en `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Descriptor raíz

La estructura de [**\_ \_ descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) declara descriptores (que aparecen en sombreadores) insertados en la firma raíz.

Este struct se utiliza cuando el tipo de ranura de firma raíz está establecido en `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` o `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Visibilidad del sombreador

El miembro de la enumeración de [**\_ \_ visibilidad del sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) establecido en el parámetro de visibilidad del sombreador del [**\_ \_ parámetro raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina qué sombreadores ven el contenido de una ranura de firma raíz determinada. Compute siempre usa \_ All (ya que solo hay una fase activa). Los gráficos pueden elegir, pero si se usan \_ todos, todas las fases del sombreador verán lo que esté enlazado en la ranura de la firma raíz.

Un uso de la visibilidad del sombreador es ayudar con los sombreadores creados que esperan enlaces diferentes por fase del sombreador mediante un espacio de nombres superpuesto. Por ejemplo, un sombreador de vértices puede declarar:

 

Texture2D foo: Register (T0); "

 

y el sombreador de píxeles también puede declarar:

 

Texture2D bar: Register (T0);

Si la aplicación realiza un enlace de firma raíz a la visibilidad de T0 \_ , ambos sombreadores verán la misma textura. Si el sombreador define realmente desea que cada sombreador vea distintas texturas, puede definir 2 ranuras de firma raíz con \_ vértices de visibilidad y \_ píxeles. Independientemente de cuál sea la visibilidad en una ranura de firma raíz, siempre tiene el mismo costo (solo en función del valor de SlotType) hacia un tamaño de firma raíz máximo fijo.

En el hardware de D3D11 de low-end, \_ también se tiene en cuenta el uso de la visibilidad del sombreador al validar los tamaños de las tablas de descriptor en un diseño raíz, ya que algunos de los hardware de D3D11 solo admiten una cantidad máxima de enlaces por fase. Estas restricciones solo se imponen cuando se ejecutan en hardware de bajo nivel y no limitan el hardware más moderno.

Si una firma raíz tiene definidas varias tablas de descriptores que se superponen entre sí en el espacio de nombres (los enlaces de registro al sombreador) y cualquiera de ellas especifica \_ All para la visibilidad, el diseño no es válido (se producirá un error en la creación).

## <a name="root-signature-definition"></a>Definición de la firma raíz

La estructura de DESC de la [**\_ \_ \_ firma raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) puede contener tablas de descriptores y constantes insertadas, cada tipo de ranura definido por la estructura de [**\_ \_ parámetros raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) y el [**\_ \_ \_ tipo de parámetro raíz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)de enumeración.

Para iniciar una ranura de firma raíz, consulte los **métodos \* \* \* SetComputeRoot** y **SetGraphicsRoot \* \* \*** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

Los muestreadores estáticos se describen en la firma raíz mediante la estructura de [**\_ \_ muestra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

Varias marcas limitan el acceso de determinados sombreadores a la firma raíz; consulte las [**marcas de \_ \_ firma raíz \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serialización/deserialización de la estructura de datos de la firma raíz

Los métodos descritos en esta sección se exportan mediante D3D12Core.dll y proporcionan métodos para serializar y deserializar una estructura de datos de firma raíz.

El formulario serializado es lo que se pasa a la API al crear una firma raíz. Si se ha creado un sombreador con una firma raíz en él (cuando se agrega esa funcionalidad), el sombreador compilado contendrá ya una firma raíz serializada.

Si una aplicación genera un procedimiento con una estructura de datos de tipo DESC de la [**\_ \_ firma \_ raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , debe crear el formulario serializado mediante [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). La salida de que se puede pasar a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Si una aplicación ya tiene una firma raíz serializada, o tiene un sombreador compilado que contiene una firma raíz y desea detectar mediante programación la definición de diseño (conocida como "reflexión"), se puede llamar a [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) . Esto genera una interfaz [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , que contiene un método para devolver la estructura de datos de DESC de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserializada. La interfaz es propietaria de la duración de la estructura de datos deserializada.

## <a name="root-signature-creation-api"></a>API de creación de firma raíz

La API [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) toma una versión serializada de una firma raíz.

## <a name="root-signature-in-pipeline-state-objects"></a>Firma raíz en objetos de estado de canalización

Los métodos para crear el estado de canalización ([**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) y [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) toman una interfaz opcional de [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) como parámetro de entrada (almacenado en una estructura de [**DESC de \_ \_ \_ estado \_ de canalización de gráficos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ). Esto invalidará cualquier firma raíz que ya esté en los sombreadores.

Si se pasa una firma raíz a uno de los métodos de creación de estado de canalización, esta firma raíz se valida con respecto a todos los Sombreadores del PSO por compatibilidad y con el controlador que se va a usar con todos los sombreadores. Si alguno de los sombreadores tiene una firma raíz diferente, se reemplaza por la firma raíz pasada en la API. Si no se pasa una firma raíz, todos los sombreadores pasados deben tener una firma raíz y deben coincidir; esto se proporcionará al controlador. La configuración de un PSO en una lista de comandos o un lote no cambia la firma raíz. Esto se logra mediante los métodos [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) y [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature). En el momento en que se invoca/dispatch (Compute), la aplicación debe asegurarse de que el PSO actual coincide con la firma raíz actual. de lo contrario, el comportamiento es indefinido.

## <a name="code-for-defining-a-version-11-root-signature"></a>Código para definir una firma raíz de la versión 1,1

En el ejemplo siguiente se muestra cómo crear una firma raíz con el siguiente formato:



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **RootParameterIndex** | **Contents**                                   |                                              |
| \[0\]                  | Constantes raíz: {B2}                         | (1 CBV)                                      |
| \[1\]                  | Tabla de descriptores: {T2-T7, U0-U3}             | (6 SRVs + 4 UAVs)                            |
| \[2\]                  | CBV raíz: {B0}                               | (1 CBV, datos estáticos)                         |
| \[3\]                  | Tabla de descriptores: {S0-S1}                    | (2 muestreadores)                                 |
| \[4\]                  | Tabla de descriptores: {T8-unbounded}           | (sin límite \# de SRVs, descriptores volátiles) |
| \[5\]                  | Tabla de descriptores: {(T0, space1)-sin enlazar} | (sin límite \# de SRVs, descriptores volátiles) |
| \[6\]                  | Tabla de descriptores: {B1}                       | (1 CBV, datos estáticos)                         |



 

Si la mayoría de las partes de la firma raíz se usan la mayor parte del tiempo, puede ser mejor que tener que cambiar la firma raíz con demasiada frecuencia. Las aplicaciones deben ordenar las entradas de la firma raíz de la que cambian con más frecuencia a menos. Cuando una aplicación cambia los enlaces a cualquier parte de la firma raíz, es posible que el controlador tenga que realizar una copia de todo o todo el estado de la firma raíz, lo que puede convertirse en un costo no trivial cuando se multiplica por muchos cambios de estado.

Además, la firma raíz definirá una muestra estática que realiza el filtrado de texturas anisotrópico en el registro del sombreador S3.

Una vez enlazada esta firma raíz, las tablas de descriptores, CBV raíz y las constantes se pueden asignar al \[ espacio de parámetros 0.. 6 \] . por ejemplo, las tablas de descriptores (rangos de un montón de descriptores) se pueden enlazar en cada uno de los parámetros raíz \[ 1 \] y \[ 3.. 6 \] .

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

En el código siguiente se muestra cómo se puede usar la firma raíz anterior en una lista de comandos de gráficos.

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

[Usar una firma raíz](using-a-root-signature.md)
</dt> </dl>

 

 
