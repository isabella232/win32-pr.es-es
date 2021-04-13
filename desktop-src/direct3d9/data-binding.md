---
description: Use la colección SasHostParameterValue para definir la colección de valores de la aplicación host, así como sus tipos y miembros, expuestos a efectos.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Enlace de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359907"
---
# <a name="data-binding"></a>Enlace de datos

Use la [colección SasHostParameterValue](#sashostparametervalue-collection) para definir la colección de valores de la aplicación host, así como sus tipos y miembros, expuestos a efectos. Use la anotación [SasBindAddress](#sasbindaddress) en un archivo de efectos para asociar un parámetro de efecto a su parámetro correspondiente en la aplicación host.

## <a name="sashostparametervalue-collection"></a>Colección SasHostParameterValue

SasHostParameterValue se define mediante la sintaxis de archivo de efectos (. FX). Aunque la sintaxis es muy similar a la sintaxis del archivo de efectos, existen algunas diferencias. Por ejemplo, los tipos de objeto, como texture2d, muestreadores y cadenas, no son válidos en los archivos de efectos reales, sino que son válidos en SasHostParameterValue. Una aplicación host puede implementar SasHostParameterValue de cualquier manera, siempre y cuando se ajuste a la descripción siguiente; la definición real se encuentra en el archivo de inclusión del efecto estándar DXSAS (/Utilities/Source/SAS/SAS.fxh de la \[ raíz del SDK \] ).

Tenga en cuenta que las matrices de SasHostParameterValue, como las luces o las cámaras, tienen una longitud sin enlazar. Esto significa que los efectos se pueden enlazar a cualquier índice arbitrario de esas matrices y las aplicaciones host deben proporcionar valores predeterminados significativos en los casos en los que no se puede proporcionar ningún valor de aplicación.

Algunos tipos y constantes deben definirse en el estándar DXSAS, como se indica en la definición de la inclusión estándar. Esto permite que los efectos enlacen fácilmente los valores agregados de SasHostParameterValue a los parámetros de efectos estructurados.



| Colección SasHostParameterValue    | Tipo            | Miembro                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [Time](#time)                       | FLOAT           | SAS. Time. Now                                 |
|                                     | FLOAT           | SAS. Time. Last                                |
|                                     | int             | SAS. Time. Númeromarco                         |
| [Mapa de entorno](#environment-map) | textureCUBE     | SAS. EnvironmentMap                           |
| [Cámara](#camera)                   | SasCamera       | SAS. Camera                                   |
|                                     | float4x4        | SAS. Camera. WorldToView                       |
|                                     | float4x4        | SAS. Camera. Projection                        |
|                                     | float2          | SAS. Camera. NearFarClipping                   |
| [Claro](#light)                     | SasAmbientLight | AmbientLight \[ ZeroOrMore \] ;                  |
|                                     | int             | SAS. NumAmbientLights                         |
|                                     | SasAmbientLight | DirectionalLight \[ ZeroOrMore \] ;              |
|                                     | int             | SAS. NumDirectionalLights                     |
|                                     | SasAmbientLight | PointLight \[ ZeroOrMore \] ;                    |
|                                     | int             | SAS. NumPointLights                           |
|                                     | SasAmbientLight | SpotLight \[ ZeroOrMore \] ;                     |
|                                     | int             | SAS. NumSpotLights                            |
| [Shadow](#shadow)                   | float4x4        | SAS. Shadow \[ ZeroOrMore \] . WorldToShadow       |
|                                     | texture2D       | SAS. Shadow \[ ZeroOrMore \] . ShadowMap           |
| [Esqueleto](#skeleton)               | float4x4        | SAS. esqueleto. MeshToJointToWorld \[ OneOrMore\] |
|                                     | int             | SAS. esqueleto. NumJoints                       |



 

### <a name="time"></a>Hora

El valor de reloj virtual o de hora de la aplicación host. Los miembros incluyen:

-   SAS. Time. Now: el valor del reloj virtual de la aplicación host en el punto en el que se representará el efecto.
-   SAS. Time. Last: el valor de Now en la representación anterior.
-   SAS. Time. Númeromarco: el valor del contador que se incrementa una vez por cada fotograma representado.

Los efectos deben controlar correctamente el hecho de que los valores de estos miembros pueden ajustarse potencialmente en los tiempos de ejecución extremadamente largos. Ahora y el último pueden tener valores muy grandes.

### <a name="environment-map"></a>Mapa de entorno

Un mapa de entorno cúbico. Las aplicaciones host deben proporcionar una textura de cubo válida si un efecto intenta enlazar a SAS. EnvironmentMap.

### <a name="camera"></a>Cámara

Cámara que se está representando actualmente. Los miembros incluyen:

-   SAS. Camera. WorldToView: la matriz de vista universal compuesta de la cámara.
-   SAS. Camera. Projection: la matriz de proyección de la cámara.
-   SAS. Camera. NearFarClipping: los valores de los planos de recorte Near y Far.

### <a name="light"></a>Claro

Una o más luces de la escena. La colección de luces se declara como una matriz donde:

-   Color: color RGB. El valor predeterminado es (0,0,0).
-   Dirección: la dirección de la luz. El valor predeterminado es (0,0,0).
-   Intervalo: la distancia desde la luz en la que los rayos de luz no tienen ningún efecto en la escena. El valor predeterminado es 0.
-   Theta: el ángulo de cono interior de un foco, medido en radianes. El valor predeterminado es 0.
-   Phi: el ángulo de cono exterior de un foco, medido en radianes. El valor predeterminado es 0.

El número de luces debe establecerse en el número de luces enlazadas a la matriz asociada. Los efectos pueden optar por omitir el número de luces y enlazar a cualquier elemento de una de las matrices ligeras. Por lo tanto, las aplicaciones host deben proporcionar un enlace válido para los elementos más allá del número de luces de la matriz.

ZeroOrMore implica que la matriz puede tener cualquier número de elementos.

### <a name="shadow"></a>Shadow

Búferes de instantáneas que constan de:

-   WorldToShadow: una matriz de matrices.
-   ShadowMap: un archivo de textura 2D.

ZeroOrMore implica que la matriz puede tener cualquier número de elementos (cero significa una matriz vacía).

Un efecto declararía una muestra de la siguiente manera:


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a>Esqueleto

Conjunto de marcos que componen el objeto que se está procesando actualmente. Los ejemplos de fotogramas son huesos y transformaciones. Esto incluye:

-   MeshToJointToWorld: una matriz de matrices.
-   NumJoints: el número de uniones en el esqueleto.

OneOrMore implica que la matriz tiene al menos un elemento y puede contener cualquier número de elementos.

La definición admite objetos de malla rígidas y estratificados mediante el mismo conjunto de valores de [colección SasHostParameterValue](#sashostparametervalue-collection) con una interpretación diferente.

## <a name="sasbindaddress"></a>SasBindAddress

Esta anotación se agrega a la parte superior de un archivo de efectos para asociar un parámetro de efecto a su parámetro correspondiente definido en la [colección SasHostParameterValue](#sashostparametervalue-collection). La anotación se declara de la siguiente manera:


```
string SasBindAddress = "SasHostParameterValue";
```



En este ejemplo se enlaza la matriz del mundo del efecto a la matriz de MeshToJointToWorld:


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



Esta anotación indica a la aplicación host que necesita establecer el valor de la matriz del efecto mundial con los datos de la matriz MeshToJointToWorld.

La sintaxis de la anotación de dirección de enlace se definió para ser muy similar a la sintaxis que usa [**ID3DXEffect**](id3dxeffect.md) para obtener y establecer los parámetros de efecto. La única diferencia entre los métodos DXSAS gramatical y **ID3DXEffect** es la adición del token de índice de asterisco. Este es otro ejemplo que usa el índice de asterisco:


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



El token de índice de asterisco denota que todos los elementos de la matriz de valores de envirnmant de host determinada (color en este caso) se deben enlazar en el parámetro asociado. Varios tokens de índice de asterisco permiten que los efectos se enlacen a subelementos de una matriz de estructuras sin necesidad de enlazar la propia estructura. En este ejemplo se enlazan los valores de color de las seis primeras luces a un parámetro de efecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de las anotaciones y semánticas estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



