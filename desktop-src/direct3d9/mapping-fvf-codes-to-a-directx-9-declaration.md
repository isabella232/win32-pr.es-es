---
description: Esta tabla asigna códigos FVF a una estructura D3DVERTEXELEMENT9.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Asignación de códigos FVF a una declaración de Direct3D 9 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85442cf1c92c78aa1a37f4d4a4ec3de154f5b8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805174"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Asignación de códigos FVF a una declaración de Direct3D 9 (Direct3D 9)

Esta tabla asigna códigos FVF a una estructura [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .



| FVF                                                   | Tipo de datos                                                           | Uso                                                                         | Índice de uso |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | \_Posición D3DDECLUSAGE                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ posición                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ FLOAT4                                                 | \_Posición D3DDECLUSAGE                                                        | 0           |
| D3DFVF \_ XYZB5 y D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 y D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT4, D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ floatn                            | \_Posición D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) y D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) y D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ normal                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ normal                                                          | 0           |
| D3DFVF \_ PSIZE                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ PSIZE                                                           | 0           |
| \_Difusión D3DFVF                                       | D3DDECLTYPE \_ D3DCOLOR                                               | COLOR de D3DDECLUSAGE \_                                                           | 0           |
| \_Reflejo D3DFVF                                      | D3DDECLTYPE \_ D3DCOLOR                                               | COLOR de D3DDECLUSAGE \_                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm (n)                              | D3DDECLTYPE \_ FLOATm                                                 | D3DDECLUSAGE \_ TEXCOORD                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Declaraciones de vértices con D3DDECLUSAGE \_ positiont

La presencia de un elemento Vertex con (D3DUSAGE \_ positiont, 0) se usa para indicar al dispositivo que los datos de vértices entran ya en el procesamiento de vértices (como un FVF con D3DFVF \_ bit XYZRHW Set). En el momento de la traza, si la declaración establecida actualmente tiene un elemento con la semántica (D3DUSAGE \_ positiont, 0), se omite todo el procesamiento de vértices (como si se hubiera establecido un FVF con D3DFVF \_ bit XYZRHW).

Existen algunas restricciones en las declaraciones de vértices con (D3DDECLUSAGE \_ positiont, 0):

-   En estas declaraciones solo se puede usar Stream 0.
-   Los elementos de vértice deben ordenarse aumentando el desplazamiento de flujo.
-   El desplazamiento del flujo debe estar alineado con DWORD.
-   El mismo par (uso, índice de uso) debe aparecer solo una vez.
-   Solo \_ se puede usar el método predeterminado D3DDECLMETHOD.
-   Otros elementos de vértice no pueden tener la \_ semántica (D3DDECLUSAGE Position, 0).

Además, hay algunas restricciones en la declaración relacionada con la versión del controlador de dispositivo. Estas restricciones están en vigor porque Direct3D envía estas declaraciones directamente al controlador sin realizar ninguna conversión.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Declaraciones de vértice sin D3DDECLUSAGE \_ positiont

El motor en tiempo de ejecución valida la creación de declaraciones. A continuación se muestran las reglas generales para las declaraciones válidas.

-   Todos los elementos de vértices de una secuencia deben ser consecutivos y ordenarse por desplazamiento.
-   El desplazamiento del flujo debe estar alineado con DWORD.
-   El mismo par (uso, índice de uso) debe aparecer solo una vez.
-   Si \_ se establece D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET
    -   Varios elementos VERTEX pueden compartir el mismo desplazamiento en una secuencia.
    -   Los elementos de vértice pueden ser de tipos diferentes, que pueden ser de diferentes tamaños.
    -   Los elementos de vértice pueden superponerse arbitrariamente. Por ejemplo, un elemento puede comenzar en una ubicación de una secuencia que es, al mismo tiempo, en el medio de otro elemento.
    -   Los elementos de vértice pueden tener el desplazamiento de la secuencia en cualquier orden.
-   El número de elementos de vértice no puede ser mayor que 64.
-   UsageIndex debe estar en el intervalo \[ 0-15 \] .
-   La declaración, que se usa con la API DrawPrimitive, no debe tener elementos de vértice distintos de D3DDECLMETHOD \_ default, D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ lookup.
-   La declaración, que contiene D3DDECLMETHOD \_ lookup o LOOKUPPRESAMPLED, solo se debe usar con la canalización de vértices programable.
-   La declaración, que se usa con la API DrawRectPatch/DrawTriPatch, no puede tener elementos de vértice con D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ lookup.
-   La declaración solo debe tener un elemento con el \_ método D3DDECLMETHOD lookup o D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La declaración con D3DDECLMETHOD \_ lookup o D3DDECLMETHOD \_ LOOKUPPRESAMPLED no debe tener elementos distintos de D3DDECLMETHOD \_ default, porque la asignación de desplazamiento se realiza solo para N-patches.
-   Los elementos de vértice con D3DDECLMETHOD \_ lookup o D3DDECLMETHOD \_ LOOKUPPRESAMPLED solo se pueden usar con la \_ semántica (D3DDECLUSAGE Sample, n) y viceversa.
-   Si un elemento de vértice con \_ el método de búsqueda D3DDECLMETHOD tiene un índice de secuencia y un desplazamiento de un elemento de vértice ya existente, este elemento de vértice debe tener el mismo tipo de datos.
-   Un elemento Vertex con el \_ método de búsqueda D3DDECLMETHOD debe tener el \_ tipo de datos D3DDECLTYPE FLOAT2/3/4
-   Los elementos de vértice con los tipos D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD \_ PARTIALU y D3DDECLMETHOD \_ PARTIALV deben tener un desplazamiento de un elemento Vertex con un tipo de datos compatible.
-   Un elemento Vertex con el método D3DDECLMETHOD \_ UV o D3DDECLMETHOD \_ LOOKUPPRESAMPLED debe tener el tipo D3DDECLTYPE sin \_ usar, el índice de flujo cero y el desplazamiento de flujo cero.
-   Las declaraciones con métodos D3DDECLMETHOD \_ UV, D3DDECLMETHOD \_ PARTIALU y D3DDECLMETHOD \_ PARTIALV solo se pueden usar con DrawRectPatch.
-   El uso \_ de D3DDECLUSAGE TESSFACTOR solo debe usarse con el tipo de datos D3DDECLTYPE \_ FLOAT1 y el índice de uso 0.
-   Cuando se usa una declaración para la teselación (DrawRectPatch, DrawTriPatch, N-patches), el tipo de datos debe ser menor o igual que D3DDECLTYPE \_ SHORT4.
-   Las declaraciones que contienen métodos que requieren ciertas funcionalidades de dispositivo (por ejemplo, la asignación de desplazamiento, RT-patches) solo se pueden crear si el dispositivo las admite.
-   Una declaración de vértice utilizada para dibujar puntos y líneas no puede tener métodos distintos de D3DDECLMETHOD \_ default.
-   Las declaraciones que se pueden crear también dependen de las capacidades del controlador.

## <a name="driver-considerations"></a>Consideraciones sobre los controladores

### <a name="pre-direct3d-9-drivers"></a>Controladores anteriores a Direct3D 9

-   La declaración de entrada debe traducirse a un FVF válido (tener el mismo orden de elementos de vértice y sus tipos de datos).
-   No se permiten espacios en las coordenadas de textura. Esto significa que si hay un elemento de vértice con (D3DDECLUSAGE \_ TEXCOORD, n), también debe haber un elemento de vértice con (D3DDECLUSAGE \_ TEXCOORD, n-1).

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Controladores de Direct3D 9 sin compatibilidad con el sombreador de píxeles versión 3

-   La declaración de entrada debe traducirse a un FVF válido (tener el mismo orden de elementos de vértice y sus tipos de datos).
-   Se permiten huecos en las coordenadas de textura.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Controladores de Direct3D 9 con compatibilidad con el sombreador de píxeles versión 3

Se permiten declaraciones más generales.

-   Los elementos de vértice pueden estar en orden arbitrario y pueden tener tipos de datos.
-   Varios elementos de vértice pueden compartir el mismo desplazamiento de flujo y ser de un tipo diferente al mismo tiempo si el \_ dispositivo establece D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Uso de la declaración de vértices con la canalización de vértices programable

-   En el tiempo de dibujo, Direct3D busca la misma combinación de "índice de uso y uso" en la declaración de vértice actual y en la función de sombreador de vértices actual. Cuando se encuentra la combinación, se usa el registro de la función de sombreador DCL como destino para el elemento de vértice.
-   Cuando un elemento de vértice en la declaración de vértice actual tiene un uso que no se encuentra en el sombreador de vértices actual, se omite ese elemento de vértice.
-   Cuando se usa una versión de sombreadores de vértices inferior a 2,0, toda la semántica mencionada en el código del sombreador debe estar presente en la declaración enlazada en tiempo de dibujo. Al usar los sombreadores de vértices 2,0 y versiones posteriores, esta restricción que permite a las aplicaciones usar declaraciones de vértices diferentes con el mismo sombreador de vértices no existe. Esto resulta útil cuando un sombreador de vértices Lee los datos de entrada en función de condiciones estáticas. El sombreador de vértices no se ha inicializado porque tendrá valores sin definir.

Hay restricciones adicionales al usar con el procesamiento de vértices de hardware en un controlador de DirectX 8:

-   Los elementos de vértice no pueden superponerse ni compartir el mismo desplazamiento.
-   Los tipos de datos se limitan a lo que el controlador DirectX 8 puede entender.

Puede producirse un error en CreateVertexDeclaration si la declaración proporcionada no se puede convertir en una declaración de estilo DirectX 8. En el caso de un dispositivo de modo mixto, este error se producirá en \* el momento de la mezcla porque es la única vez que se puede saber si este sombreador se usa con el procesamiento de vértices de hardware o software.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Uso de la declaración de vértices con la canalización de funciones fijas

Solo se pueden usar las declaraciones que cumplan las siguientes reglas:

-   No debe haber huecos entre los elementos de vértice (no se permitía OMITIr en una declaración de DirectX 8, que se usa para la canalización de función fija).
-   \_Se debe especificar Semantic (D3DDECLUSAGE Position, 0) y debe tener D3DDECLTYPE \_ FLOAT3 Data Type.
-   Un elemento Vertex con el método D3DDECLMETHOD \_ UV debe especificar Usage D3DDECLUSAGE \_ TEXCOORD o D3DDECLUSAGE \_ BLENDWEIGHT.
-   Un elemento Vertex con el método D3DDECLMETHOD \_ PARTIALU, \_ PARTIALV o \_ CROSSUV solo se puede usar con D3DDECLUSAGE \_ Position, \_ normal, \_ BLENDWEIGHT o \_ TEXCOORD y debe usar el tipo de entrada D3DDECLTYPE \_ FLOAT3.

Cuando se usa una declaración con el procesamiento de vértices de hardware en un controlador de DirectX 8, el tiempo de ejecución de Direct3D lo convierte en una declaración de estilo de DirectX 8 con las siguientes reglas:

-   Los elementos de vértice no pueden compartir el mismo desplazamiento en una secuencia y no pueden superponerse.
-   El tipo de datos debe ser menor o igual que D3DDECLTYPE \_ SHORT4.
-   Solo se permiten los siguientes métodos: D3DDECLMETHOD \_ default, D3DDECLMETHOD \_ CROSSUV y D3DDECLMETHOD \_ UV
-   La [asignación entre una declaración de Direct3D 9 y una declaración de Direct3D 8 (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) muestra qué semántica de Direct3D 9 se puede convertir en una declaración de estilo de DirectX 8. Usage y UsageIndex se convierten en un valor de registro.
-   Si hay n elementos de vértice en una declaración y 0-m (m < n) se asigna a un FVF (elementos descritos en la [asignación entre una declaración de Direct3D y códigos de FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)), pero m + 1 no lo hace:
    -   Si cualquiera de los elementos de vértice de m + 2 se asignan a FVF/dx8decl, la declaración no es válida.
    -   Los elementos 0 a m se convierten (por el tiempo de ejecución para los controladores de DirectX 8 y anteriores, y los controladores de Direct3D 9) mediante la [asignación entre una declaración de Direct3D y códigos de FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md), m + 1, m + 2 hasta que n-1 se asigna a texcoord (k) contiguos, texcoord (k + 1), a partir de cualquier
    -   Se supone que el tipo de datos de una texcoord asignada es Float \[ 1234 \] , reemplazando cualquier tipo de datos que contenga el elemento actual (pero con el mismo tamaño). Por lo tanto, el tipo de datos existente puede ser algo que no está en la [asignación entre una declaración de Direct3D y códigos de FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md).
    -   Si k llega a 8, la declaración no es válida para FVF/dx8decl.
    -   Si se ha producido alguna asignación a texcoords, se requiere que la declaración completa no tenga ningún elemento con un método de generación distinto de DEFAULT o que la declaración no sea válida para FVF/dx8decl.

## <a name="using-vertex-declarations-with-processvertices"></a>Usar declaraciones de vértices con ProcessVertices

Se puede usar una declaración de vértice para describir el resultado de ProcessVertices. Esta declaración debe cumplir las siguientes reglas:

-   Solo se debe usar la secuencia 0.
-   Solo \_ se permiten los métodos predeterminados de D3DDECLMETHOD.
-   Solo \_ se pueden usar los tipos de datos D3DDECLTYPE floatn o D3DDECLTYPE \_ D3DCOLOR.
-   Los elementos de vértice no pueden compartir el mismo desplazamiento o superponerse entre sí.
-   Los elementos de vértice con (D3DDECLUSAGE \_ Position, 0) o (D3DDECLUSAGE \_ positiont, 0) no son necesarios.
-   Los elementos de vértice con (D3DDECLUSAGE \_ Position, 0) y (D3DDECLUSAGE \_ positiont, 0) no pueden estar presentes en la misma declaración.
-   El sombreador de vértices actual debe ser de la versión 3,0 o superior cuando se usa dicha declaración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 



