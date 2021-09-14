---
description: Esta tabla asigna códigos FVF a una estructura D3DVERTEXELEMENT9.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Asignación de códigos FVF a una declaración de Direct3D 9 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85442cf1c92c78aa1a37f4d4a4ec3de154f5b8d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966607"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Asignación de códigos FVF a una declaración de Direct3D 9 (Direct3D 9)

Esta tabla asigna códigos FVF a una [**estructura D3DVERTEXELEMENT9.**](d3dvertexelement9.md)



| FVF                                                   | Tipo de datos                                                           | Uso                                                                         | Índice de uso |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | POSICIÓN DE D3DDECLUSAGE \_                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITIONT                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ FLOAT4                                                 | POSICIÓN DE D3DDECLUSAGE \_                                                        | 0           |
| D3DFVF \_ XYZB5 y D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 y D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT4, D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOATn                            | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n=1..4) y D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4) y D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ NORMAL                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ NORMAL                                                          | 0           |
| D3DFVF \_ PSIZE                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ PSIZE                                                           | 0           |
| D3DFVF \_ DIFUSO                                       | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE \_ COLOR                                                           | 0           |
| ESPECULAR D3DFVF \_                                      | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE \_ COLOR                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm(n)                              | D3DDECLTYPE \_ FLOATm                                                 | D3DDECLUSAGE \_ TEXCOORD                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Declaraciones de vértices con D3DDECLUSAGE \_ POSITIONT

La presencia de un elemento de vértice con (D3DUSAGE POSITIONT, 0) se usa para indicar al dispositivo que los datos de vértice que llegan ya han sido a través del procesamiento de vértices (como FVF con conjunto de bits \_ D3DFVF \_ XYZRHW). En tiempo de dibujo, si la declaración establecida actualmente tiene un elemento con la semántica (D3DUSAGE POSITIONT, 0), se omite todo el procesamiento de vértices (como si se hubiera establecido un bit FVF con \_ D3DFVF \_ XYZRHW).

Hay algunas restricciones en las declaraciones de vértices con (D3DDECLUSAGE \_ POSITIONT, 0):

-   Solo se puede usar el flujo cero en estas declaraciones.
-   Los elementos de vértice deben ordenarse aumentando el desplazamiento de flujo.
-   El desplazamiento de flujo debe estar alineado con DWORD.
-   El mismo par (Uso, Índice de uso) solo debe aparecer una vez.
-   Solo se puede usar el método D3DDECLMETHOD \_ DEFAULT.
-   Otros elementos de vértice no pueden tener la semántica (D3DDECLUSAGE \_ POSITION, 0).

Además, hay algunas restricciones en esta declaración relacionadas con la versión del controlador de dispositivo. Estas restricciones están en vigor porque Direct3D envía estas declaraciones directamente al controlador sin realizar ninguna conversión.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Declaraciones de vértices sin D3DDECLUSAGE \_ POSITIONT

Runtime valida la creación de declaraciones. A continuación se den las reglas generales para las declaraciones que son legales.

-   Todos los elementos de vértice de una secuencia deben ser consecutivos y ordenarse por desplazamiento.
-   El desplazamiento de flujo debe estar alineado con DWORD.
-   El mismo par (Uso, Índice de uso) solo debe aparecer una vez.
-   Si D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET está establecido,
    -   Varios elementos de vértice pueden compartir el mismo desplazamiento en una secuencia.
    -   Todos los elementos de vértice pueden ser de tipos diferentes que pueden ser de diferentes tamaños.
    -   Los elementos de vértice se pueden superponer arbitrariamente. Por ejemplo, un elemento puede comenzar en una ubicación de una secuencia que, al mismo tiempo, se encuentra en medio de otro elemento.
    -   Los elementos de vértice pueden tener desplazamiento de flujo en cualquier orden.
-   El número de elementos de vértice no puede ser mayor que 64.
-   UsageIndex debe estar en el intervalo \[ 0-15. \]
-   La declaración, que se usa con DrawPrimitive API, no debe tener elementos de vértice distintos de D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ LOOKUP.
-   La declaración, que contiene D3DDECLMETHOD LOOKUP o LOOKUPPRESAMPLED, solo se debe usar con la \_ canalización de vértices programable.
-   La declaración, que se usa con la API DrawRectPatch/DrawTriPatch, no puede tener elementos de vértice con D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ LOOKUP.
-   La declaración solo debe tener un elemento con el método D3DDECLMETHOD \_ LOOKUP o D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La declaración con D3DDECLMETHOD LOOKUP o D3DDECLMETHOD LOOKUPPRESAMPLED no debe tener elementos distintos de \_ \_ D3DDECLMETHOD DEFAULT, ya que la asignación de desplazamiento solo se realiza para \_ N revisiones.
-   Los elementos de vértice con D3DDECLMETHOD LOOKUP o D3DDECLMETHOD LOOKUPPRESAMPLED solo se pueden usar con la semántica \_ \_ (D3DDECLUSAGE \_ SAMPLE, n) y viceversa.
-   Si un elemento de vértice con el método D3DDECLMETHOD LOOKUP tiene un índice de flujo y un desplazamiento de un elemento de vértice ya existente, este elemento de vértice debe \_ tener el mismo tipo de datos.
-   Un elemento de vértice con el método D3DDECLMETHOD LOOKUP debe tener el tipo de datos \_ D3DDECLTYPE \_ FLOAT2/3/4
-   Los elementos de vértice con los tipos D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD PARTIALU y \_ D3DDECLMETHOD PARTIALV deben tener un desplazamiento de un elemento de vértice con un tipo de datos \_ compatible.
-   Un elemento de vértice con el método D3DDECLMETHOD UV o \_ D3DDECLMETHOD LOOKUPPRESAMPLED debe tener el tipo \_ D3DDECLTYPE UNUSED, el índice de flujo cero y el desplazamiento de flujo \_ cero.
-   Las declaraciones con los métodos D3DDECLMETHOD \_ UV, D3DDECLMETHOD PARTIALU y D3DDECLMETHOD PARTIALV solo se pueden usar con \_ \_ DrawRectPatch.
-   Usage D3DDECLUSAGE TESSFACTOR debe usarse solo con el tipo de datos \_ D3DDECLTYPE FLOAT1 y el índice \_ de uso 0.
-   Cuando se usa una declaración para la teselación (DrawRectPatch, DrawTriPatch, N-patches), el tipo de datos debe ser menor o igual que D3DDECLTYPE \_ SHORT4.
-   Las declaraciones que contienen métodos que requieren ciertas funcionalidades de dispositivo (por ejemplo, asignación de desplazamiento o revisiones RT) solo se pueden crear si el dispositivo las admite.
-   Una declaración de vértice utilizada para dibujar puntos y líneas no puede tener métodos distintos de D3DDECLMETHOD \_ DEFAULT.
-   Las declaraciones que se pueden crear también dependen de las funcionalidades del controlador.

## <a name="driver-considerations"></a>Consideraciones sobre el controlador

### <a name="pre-direct3d-9-drivers"></a>Controladores de Pre-Direct3D 9

-   La declaración de entrada debe ser traducible a una FVF válida (tener el mismo orden de elementos de vértice y sus tipos de datos).
-   No se permiten espacios en las coordenadas de textura. Esto significa que si hay un elemento de vértice con (D3DDECLUSAGE TEXCOORD, n), también debe haber un elemento de vértice con \_ (D3DDECLUSAGE \_ TEXCOORD, n-1).

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Controladores de Direct3D 9 sin compatibilidad con sombreador de píxeles versión 3

-   La declaración de entrada debe ser traducible a una FVF válida (tener el mismo orden de elementos de vértice y sus tipos de datos).
-   Se permiten espacios en las coordenadas de textura.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Controladores de Direct3D 9 con compatibilidad con sombreador de píxeles versión 3

Se permiten declaraciones más generales.

-   Los elementos de vértice pueden estar en orden arbitrario y pueden tener cualquier tipo de datos.
-   Varios elementos de vértice pueden compartir el mismo desplazamiento de flujo y ser de un tipo diferente al mismo tiempo si el dispositivo establece D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Uso de declaraciones de vértices con la canalización de vértices programables

-   En el momento del dibujo, Direct3D busca la misma combinación de "uso- índice de uso" en la declaración de vértice actual y la función actual del sombreador de vértices. Cuando se encuentra la combinación, el registro de la función de sombreador DCL se usa como destino del elemento de vértice.
-   Cuando un elemento de vértice de la declaración de vértice actual tiene un uso que no se encuentra en el sombreador de vértices actual, ese elemento de vértice se omite.
-   Cuando se usa una versión de sombreador de vértices inferior a 2.0, toda la semántica mencionada en el código del sombreador debe estar presente en la declaración enlazada en tiempo de dibujo. Cuando se usan sombreadores de vértices 2.0 y versiones posteriores, esta restricción que permite a las aplicaciones usar declaraciones de vértices diferentes con el mismo sombreador de vértices no existe. Esto resulta útil cuando un sombreador de vértices lee los datos de entrada en función de condiciones estáticas. Los registros del sombreador de vértices no inicializados debido a esto tendrán valores indefinidos.

Hay restricciones adicionales al usar con el procesamiento de vértices de hardware en un controlador DirectX 8:

-   Los elementos de vértice no se pueden superponer ni compartir el mismo desplazamiento.
-   Los tipos de datos se limitan a lo que el controlador DirectX 8 puede entender.

CreateVertexDeclaration podría producir un error si la declaración proporcionada no se puede convertir en una declaración de estilo DirectX 8. En el caso de un dispositivo en modo mixto, este error se produce en tiempo de dibujo porque es la única vez que se puede saber si este sombreador se usa con el procesamiento de vértices de hardware o \* software.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Uso de declaraciones de vértices con la canalización de función fija

Solo se pueden usar declaraciones que cumplan las reglas siguientes:

-   No debería haber espacios entre los elementos de vértice (no se permitió SKIP en una declaración de DirectX 8, que se usa para la canalización de funciones fijas).
-   Se debe especificar la semántica (D3DDECLUSAGE POSITION, 0) y debe tener el tipo de datos \_ D3DDECLTYPE \_ FLOAT3.
-   Un elemento de vértice con el método D3DDECLMETHOD UV debe especificar el uso \_ D3DDECLUSAGE \_ TEXCOORD o D3DDECLUSAGE \_ BLENDWEIGHT.
-   Un elemento de vértice con el método D3DDECLMETHOD PARTIALU, PARTIALV o CROSSUV solo se puede usar con \_ \_ D3DDECLUSAGE POSITION, NORMAL, BLENDWEIGHT o TEXCOORD, y debe usar el tipo de \_ \_ entrada \_ \_ \_ D3DDECLTYPE \_ FLOAT3.

Cuando se usa una declaración con el procesamiento de vértices de hardware en un controlador DirectX 8, el tiempo de ejecución de Direct3D la convierte en una declaración de estilo DirectX 8 con las reglas siguientes:

-   Los elementos de vértice no pueden compartir el mismo desplazamiento en una secuencia y no se pueden superponer.
-   El tipo de datos debe ser menor o igual que D3DDECLTYPE \_ SHORT4.
-   Solo se permiten los métodos siguientes: D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD CROSSUV y \_ D3DDECLMETHOD \_ UV
-   La asignación entre una declaración de Direct3D 9 y una declaración [de Direct3D 8 (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) muestra qué semántica de Direct3D 9 se podría convertir en declaración de estilo DirectX 8. Usage y UsageIndex se convierten en un valor de registro.
-   Si hay n elementos de vértice en una declaración y 0 - m (m < n) se asigna a una FVF (elementos descritos en asignación entre una declaración de Direct3D y códigos [FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)), pero m + 1 no, entonces:
    -   Si cualquiera de m + 2 hasta n - 1 los elementos de vértice se asignan a FVF/dx8decl, la declaración no es válida.
    -   Los elementos de 0 a m se convierten (por el tiempo de ejecución para DirectX 8 y controladores más antiguos, y por los controladores de Direct3D 9) mediante la asignación entre una declaración de Direct3D y códigos [FVF (Direct3D 9),](mapping-between-a-directx-9-declaration-and-fvf-codes.md)m + 1, m + 2 hasta n - 1 se asignan a contiguos de la declaración de Direct3D y los códigos FVF (k+1), empezando desde cualquier elemento de los elementos 0 a m.
    -   Se supone que el tipo de datos de un objeto texcoord asignado es float 1234, reemplazando el tipo de datos que contiene el elemento actual \[ \] (pero con el mismo tamaño). Por lo tanto, el tipo de datos existente puede ser algo que no está en Asignación entre una declaración de Direct3D y códigos [FVF (Direct3D 9).](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
    -   Si k alcanza 8, la declaración no es válida para FVF/dx8decl.
    -   Si se ha producido alguna asignación a los tipos, es necesario que toda la declaración no tenga ningún elemento con un método de generación distinto de DEFAULT o que la declaración no sea válida para FVF/dx8decl.

## <a name="using-vertex-declarations-with-processvertices"></a>Usar declaraciones de vértice con ProcessVertices

Se podría usar una declaración de vértice para describir la salida de ProcessVertices. Dicha declaración debe cumplir las reglas siguientes:

-   Solo se debe usar el flujo 0.
-   Solo se permiten métodos D3DDECLMETHOD \_ DEFAULT.
-   Solo se pueden usar los tipos de datos D3DDECLTYPE \_ FLOATn o D3DDECLTYPE \_ D3DCOLOR.
-   Los elementos de vértice no pueden compartir el mismo desplazamiento ni superponerse entre sí.
-   No se requieren elementos de vértice con (D3DDECLUSAGE \_ POSITION, 0) o (D3DDECLUSAGE \_ POSITIONT,0).
-   Los elementos de vértice con (D3DDECLUSAGE \_ POSITION, 0) y (D3DDECLUSAGE POSITIONT,0) no pueden estar \_ presentes en la misma declaración.
-   El sombreador de vértices actual debe tener la versión 3.0 o posterior cuando se usa dicha declaración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 



