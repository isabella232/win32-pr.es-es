---
description: Al transferir valores entre la aplicación host y un parámetro de efecto, los datos se escriben de la manera esperada cuando el tipo de datos de origen (en la aplicación host) coincide con el tipo de datos de destino (en el parámetro Effect).
ms.assetid: 4f3ef14a-7d67-45fe-9282-541221815d1f
title: Conversión y conversión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b8ab6ec3fccd8dc57d503de18ffe1e9e321377
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153060"
---
# <a name="casting-and-conversion"></a>Conversión y conversión

Al transferir valores entre la aplicación host y un parámetro de efecto, los datos se escriben de la manera esperada cuando el tipo de datos de origen (en la aplicación host) coincide con el tipo de datos de destino (en el parámetro Effect). Cuando los tipos de datos difieren, la conversión se realizará cuando los datos de origen se reorganicen para ajustarse al destino.

DXSAS define las siguientes reglas de conversión de tipos. Son un superconjunto de las reglas de conversión de tipo de efecto (. FX) y HLSL. DXSAS también define algunos [modificadores de valor de parámetro](#parameter-value-modifiers) que pueden afectar al valor que se transfiere desde la aplicación host a un parámetro enlazado.

## <a name="type-casting"></a>Conversión de tipos

En la tabla siguiente se muestra la conversión que se produce cuando se transfiere un tipo de datos a otro tipo de datos:



| Tipo de origen                                  | Tipo de destino                             | Comportamiento                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLOAT                                        | int                                          | Redondeo a cero.                                                                                                                                                                                                                                                                                                                                                                                      |
| Float, int                                   | bool                                         | Los valores que no son iguales a 0: basados en una comparación no igual a 0 (int) o 0,0 (float), se consideran verdaderos; de lo contrario, se considera que el valor es false.                                                                                                                                                                                                                                         |
| int                                          | FLOAT                                        |                                                                                                                                                                                                                                                                                                                                                                                                          |
| bool                                         | int, float                                   | False se convierte en cero. True se convierte en uno.                                                                                                                                                                                                                                                                                                                                                     |
| texture1D, texture2D, texture3D, textureCUBE | textura                                      | La textura de destino se trata como el tipo de textura de origen.                                                                                                                                                                                                                                                                                                                                               |
| string                                       | texture1D, texture2D, texture3D, textureCUBE | El valor de cadena se trata como una dirección de recurso y se resuelve de la misma manera que la [anotación de inicialización de parámetros](parameter-initialization-annotation.md). Si no se puede resolver la dirección del recurso, la conversión no es válida y las aplicaciones host deben devolver un error. Si el recurso se resuelve correctamente, el tipo de la expresión se trata como el mismo tipo que el recurso resuelto. |



 

## <a name="class-casting"></a>Conversión de clases

Además de las reglas de conversión de tipos descritas anteriormente, DXSAS define el conjunto de reglas de conversión necesarias para realizar la conversión entre tipos de clase. Las matrices de columnas (N x 1), las matrices de filas (1 x N) y las estructuras numéricas se tratan como vectores.

Los parámetros de la matriz de efectos y las variables de matriz de HLSL pueden definir si el valor es una matriz principal de filas o de columnas principales; sin embargo, las API de DirectX siempre tratan [**D3DMATRIX**](d3dmatrix.md) y [**D3DXMATRIX**](d3dxmatrix.md) como fila principal.



| Clase de origen | Clase de destino | Comportamiento                                                                                                                                                                                                                                                                                                                                        |
|--------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escalar       | Escalar            | Aplicar conversión de tipos.                                                                                                                                                                                                                                                                                                                             |
| Escalar       | Vector            | Replique el valor de origen escalar en todos los componentes del vector de destino después de aplicar la conversión de tipos y el comportamiento de conversión descritos en conversión de tipos.                                                                                                                                                                             |
| Escalar       | Matrix            | Replique el valor de origen escalar en todos los componentes de la matriz de destino después de aplicar la conversión de tipos y el comportamiento de conversión descritos en conversión de tipos.                                                                                                                                                                             |
| Escalar       | Object            | Conversión no válida. Las aplicaciones host deben devolver un error.                                                                                                                                                                                                                                                                                           |
| Escalar       | Estructura         | Solo es válido si la estructura de destino contiene solo elementos numéricos. Si es válido, replique el valor de origen escalar en todos los componentes de la estructura de destino después de aplicar la conversión de tipos y el comportamiento de conversión descritos en conversión de tipos.                                                                                        |
| Vector       | Escalar            | El escalar de destino recibe el valor del primer componente del vector de origen después de aplicar la conversión de tipos y el comportamiento de conversión descritos en [conversión de tipos](#type-casting).                                                                                                                                                       |
| Vector       | Vector            | Conversión no válida si el vector de destino tiene más componentes que el vector de origen. El vector de destino recibe los valores más a la izquierda del vector de origen después de aplicar la conversión de tipos y el comportamiento de conversión descritos en [conversión de tipos](#type-casting). Se pierden los demás componentes del vector de origen restantes.             |
| Vector       | Matrix            | Conversión no válida a menos que el vector de origen tenga el mismo número de componentes que la matriz de destino. Si la conversión es válida, se aplica el comportamiento de la conversión de vector a vector.                                                                                                                                                             |
| Vector       | Object            | Conversión no válida. Las aplicaciones host deben devolver un error.                                                                                                                                                                                                                                                                                           |
| Vector       | Estructura         | Solo es válido si la estructura de destino solo tiene elementos numéricos y no contiene más elementos de los que el vector de origen tiene componentes. Los elementos de la estructura de destino reciben los componentes de la parte izquierda del vector de origen después de aplicar la conversión de tipos y el comportamiento de conversión descritos en [conversión de tipos](#type-casting).      |
| Matrix       | Escalar            | El escalar de destino recibe el valor del valor situado en la parte superior izquierda de la matriz de origen después de aplicar la conversión de tipos y el comportamiento de conversión descritos en [conversión de tipos](#type-casting).                                                                                                                                                 |
| Matrix       | Vector            | Conversión no válida a menos que la matriz de origen tenga el mismo número de componentes que el vector de destino. Si la conversión es válida, se aplica el comportamiento de la conversión de vector a Vector anterior.                                                                                                                                                       |
| Matrix       | Matrix            | Conversión no válida si la matriz de destino tiene más componentes que la matriz de origen. La matriz de destino recibe los valores superiores izquierdos de la matriz de origen después de aplicar la conversión de tipos y el comportamiento de conversión descritos en [conversión de tipos](#type-casting). Se pierden los componentes restantes que se encuentran más a la derecha de la matriz de origen. |
| Matrix       | Object            | Conversión no válida. Las aplicaciones host deben devolver un error.                                                                                                                                                                                                                                                                                           |
| Matrix       | Estructura         | El tamaño de la estructura debe ser igual al tamaño de la matriz y todos los componentes de la estructura deben ser numéricos.                                                                                                                                                                                                                          |
| Object       | Escalar            | Conversión no válida. Las aplicaciones host deben devolver un error.                                                                                                                                                                                                                                                                                           |
| Object       | Vector            | Conversión no válida. Las aplicaciones host deben devolver un error.                                                                                                                                                                                                                                                                                           |
| Object       | Matrix            | Conversión no válida. Las aplicaciones host deben devolver un error.                                                                                                                                                                                                                                                                                           |
| Object       | Object            | Válido si los tipos de los objetos son idénticos y de acuerdo con el comportamiento definido en la [conversión de tipos](#type-casting).                                                                                                                                                                                                                   |
| Estructura    | Escalar            | Válido si la estructura de origen contiene al menos un miembro numérico. El escalar de destino recibe el valor del primer miembro numérico de la estructura de origen después de aplicar la conversión de tipos y el comportamiento de conversión descritos en [conversión de tipos](#type-casting).                                                                                |
| Estructura    | Vector            | La estructura de origen debe ser al menos el tamaño del vector. Los primeros componentes deben ser numéricos hasta el tamaño del vector de destino.                                                                                                                                                                                                    |
| Estructura    | Matrix            | La estructura de origen debe ser al menos el tamaño del vector. Los primeros componentes deben ser numéricos hasta el tamaño del vector de destino.                                                                                                                                                                                                    |
| Estructura    | Estructura         | La estructura de destino no debe ser mayor que la estructura de origen. Debe existir una conversión válida entre todos los componentes de origen y de destino respectivos.                                                                                                                                                                                       |



 

## <a name="parameter-value-modifiers"></a>Modificadores de valor de parámetro

Las anotaciones del modificador de parámetro agregan información adicional a un parámetro para que los datos del parámetro se puedan interpretar correctamente. Por ejemplo, puede que sea necesario expresar un vector con datos normalizados o que se mida una longitud en pulgadas. Las anotaciones del modificador de valor de parámetro expresan esta información adicional para que las aplicaciones host puedan transformar los valores correctamente cuando los datos se transfieran a un parámetro de efecto.

Estos son los modificadores de parámetro:



| Anotaciones del modificador de valor de parámetro | Descripción                                    |
|--------------------------------------|------------------------------------------------|
| [SasNormalize](#sasnormalize)        | Especifique si un vector está normalizado o no. |
| [SasUnits](#sasunits)                | Especifique las unidades de medida de un parámetro.  |



 

### <a name="sasnormalize"></a>SasNormalize

La anotación SasNormalize denota que el parámetro asociado debe ser un valor normalizado cada vez que se asigna. Esta anotación solo afecta a los parámetros float2, float3 y FLOAT4.


```
string SasNormalize = "Value";
```



donde value es true o false.

Este es un ejemplo:


```
float3 UpNormal
<
  bool SasNormalize = "True";
>;
```



### <a name="sasunits"></a>SasUnits

Los datos de los parámetros de efecto están en las siguientes unidades:


```
string SasUnits = "Value";
```



donde value es uno de los siguientes:



| Tipo de medida     | Value        | Descripción                    |
|----------------------|--------------|--------------------------------|
| Sin unidades             | cadena vacía | Sin unidades                       |
| Distancia             | MM           | Milímetros                    |
|                      | cm           | Centímetros                    |
|                      | m            | Metros                         |
|                      | km           | Kilómetros                     |
| Ángulo                | rad          | Radians                        |
| Hora                 | ms           | Milisegundos                   |
|                      | seg.          | Segundos                        |
|                      | min.          | Minutos                        |
|                      | h           | Horas                          |
| Velocidad lineal      | mm/s       | Milímetros por segundo         |
|                      | cm/s       | Centímetros por segundo         |
|                      | m/s        | Medidores por segundo              |
|                      | m/h         | Medidores por hora                |
|                      | km/h        | Kilómetros por hora            |
| Aceleración lineal  | mm/s ²      | Milímetros por segundo cuadrado |
|                      | cm/s ²      | Centímetros por segundo al cuadrado |
|                      | m/s ²       | Medidores por segundo cuadrado      |
|                      | m/h ²        | Medidores por hora cuadrado        |
|                      | km/h ²       | Kilómetros por hora al cuadrado    |
| Velocidad angular     | rad/s      | Radianes por segundo             |
| Aceleración angular | rad/s ²     | Radianes por segundo cuadrado     |
| Área                 | mm ²          | Milímetros cuadrados            |
|                      | cm ²          | Centímetros al cuadrado            |
|                      | m           | Medidores cuadrados                 |
|                      | km²          | Kilómetros cuadrados             |
| Volumen               | mm ³          | Milímetros con cubo              |
|                      | cm          | Centímetros con cubos              |
|                      | diarios           | Medidores con cubo                   |
|                      | km ³          | Kilómetros con cubo               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de las anotaciones y semánticas estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



