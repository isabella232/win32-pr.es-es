---
description: Transición de borrado de SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transición de borrado de SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47de62c450ff0d75f72e5fac466801991b987834
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275159"
---
# <a name="smpte-wipe-transition"></a>Transición de borrado de SMPTE

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La transición de borrado de SMPTE genera cualquiera de los borrados estándar definidos por la Society of Motion Picture and Tv Engineers (SMPTE) en el documento 258M-1993 de SMPTE, a excepción de la división de cuatro.

![transición de borrado en curso](images/trans-wipe.png)

Id. de clase (CLSID): {DE75D012-7A65-11D2-8ATTRIBUTE-00A0C9441E20}

Nombre de la variable CLSID: CLSID \_ DxtMideg

Nombre descriptivo: "DxtXtXteg"

Propiedades



| Propiedad.       | Tipo   | Valor predeterminado  | Descripción                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Color del borde alrededor de los bordes del patrón de borrado. El valor de este atributo es un número hexadecimal con el formato 0x *RRGGBB,* donde *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul. (Por lo tanto, el rojo puro, el verde y el azul se 0xFF000, 0x00FF00 y 0x0000FF, respectivamente). |
| BorderSoftness | long   | 0        | Ancho de la región desenfoque alrededor de los bordes del patrón de borrado. Especifique cero para ninguna región desenfoque.                                                                                                                                                                                                              |
| BorderWidth    | long   | 0        | Ancho del borde sólido a lo largo de los bordes del patrón de borrado. Especifique cero para ningún borde.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Si no **es NULL,** especifica el nombre de un archivo JPEG que se usará como máscara de borrado en lugar de un borrado estándar integrado. El archivo debe contener un degradado monocromo de 8 bits por píxel. El degradado se usa como máscara para definir la progresión del borrado.                                                                 |
| MaskNum        | long   | 1        | Código de borrado SMPTE estándar que especifica el estilo de borrado que se va a usar. Para obtener una lista de códigos de borrado y sus esquemas asociados, vea el documento 258M-1993 de SMPTE.                                                                                                                                                            |
| OffsetX        | long   | 0        | Desplazamiento horizontal del origen de borrado desde el centro de la imagen. Válido solo para los valores **de MaskNum** de 101 a 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Desplazamiento verical del origen de borrado desde el centro de la imagen. Válido solo para los valores **de MaskNum** de 101 a 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Número de veces que se replica el patrón de borrado horizontalmente. Válido solo para los valores **de MaskNum** de 101 a 131.                                                                                                                                                                                                |
| Replicación     | long   | 0        | Número de veces que se replica el patrón de borrado verticalmente. Válido solo para los valores **de MaskNum** de 101 a 131.                                                                                                                                                                                                  |
| Scalex         | double | 1.0      | Cantidad por la que se va a extender el borrado horizontalmente, como un porcentaje de la definición de borrado original. Válido solo para los valores **de MaskNum** de 101 a 131.                                                                                                                                                         |
| Scaley         | double | 1.0      | Cantidad por la que se va a extender el borrado verticalmente, como un porcentaje de la definición de borrado original. Válido solo para los valores **de MaskNum** de 101 a 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

Esta transición admite los siguientes borrados SMPTE estándar:



| Number | Descripción                   | Number | Descripción                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radial, izquierda-derecha, superior                     |
| 2      | Vertical                      | 212    | Radial, arriba hacia abajo, derecha                      |
| 3      | Parte superior izquierda                    | 213    | Radial, izquierda-derecha, superior inferior              |
| 4      | Esquina superior derecha                   | 214    | Radial, arriba hacia abajo, izquierda-derecha                 |
| 5      | Inferior derecha                   | 221    | Radial, superior                                 |
| 6      | Inferior izquierda                    | 222    | Radial, derecha                               |
| 7      | Cuatro esquinas                  | 223    | Radial, inferior                              |
| 8      | Cuatro cuadrados                  | 224    | Radial, izquierda                                |
| 21     | Puertas de cristal, verticales          | 225    | Radial, superior en el sentido de las agujas del reloj, inferior en el sentido de las agujas del reloj     |
| 22     | Puertas traseras, horizontales        | 226    | Radial, izquierda en el sentido de las agujas del reloj, derecha en el sentido de las agujas del reloj     |
| 23     | Centro superior                    | 227    | Radial, superior en el sentido de las agujas del reloj, inferior en el sentido de las agujas del reloj |
| 24     | Centro derecho                  | 228    | Radial, izquierda en el sentido de las agujas del reloj, derecha en el sentido de las agujas del reloj |
| 25     | Centro inferior                 | 231    | Radial, división superior                           |
| 26     | Centro izquierdo                   | 232    | Radial, división a la derecha                         |
| 41     | Diagonal, NW a SE            | 233    | Radial, división inferior                        |
| 42     | Diagonal, NE a SW            | 234    | Radial, división izquierda                          |
| 43     | Triángulos, superior e inferior         | 235    | Radial, división de arriba abajo                    |
| 44     | Triángulos, izquierda/derecha         | 236    | Radial, división izquierda-derecha                    |
| 45     | Franja diagonal, de SW a NE     | 241    | Radial, esquina superior izquierda                     |
| 46     | Franja diagonal, NW a SE     | 242    | Radial, esquina inferior izquierda                  |
| 47     | Cross                         | 243    | Radial, esquina inferior derecha                 |
| 48     | Diamond Box                   | 244    | Radial, esquina superior derecha                    |
| 61     | Condón, parte superior                    | 245    | Radial, superior izquierda, inferior derecha              |
| 62     | Conste, derecho                  | 246    | Radial, inferior izquierda, superior derecha              |
| 63     | Fondo, parte inferior                 | 251    | Radial central, superior                          |
| 64     | Verón, izquierda                   | 252    | Radial central, izquierda                         |
| 65     | V                             | 253    | Radial central, inferior                       |
| 66     | V, derecha                      | 254    | Radial central, derecha                        |
| 67     | V, invertido                   | 261    | Radial box, right                           |
| 68     | V, izquierda                       | 262    | Radial box, top                             |
| 71     | Sawtooth, left                | 263    | Radial central, superior e inferior                  |
| 72     | Sawtooth, top                 | 264    | Radial central, izquierda, derecha                  |
| 73     | Sawtooth, vertical            | 301    | Matriz, horizontal                          |
| 74     | Sawtooth, horizontal          | 302    | Matriz, vertical                            |
| 101    | Cuadro                           | 303    | Matriz, diagonal, superior izquierda                  |
| 102    | Diamond                       | 304    | Matriz, diagonal, superior derecha                 |
| 103    | Triángulo, arriba                  | 305    | Matriz, diagonal, inferior derecha              |
| 104    | Triángulo, derecha               | 306    | Matriz, diagonal, inferior izquierda               |
| 105    | Triángulo, parte inferior              | 310    | Matriz, esquina superior izquierda en el sentido de las agujas del reloj                  |
| 106    | Triángulo, izquierda                | 311    | Matriz, esquina superior derecha en el sentido de las agujas del reloj                 |
| 107    | Flecha arriba                | 312    | Matriz, esquina inferior derecha en el sentido de las agujas del reloj              |
| 108    | Dirección de flecha, derecha             | 313    | Matriz, esquina inferior izquierda en el sentido de las agujas del reloj               |
| 109    | Flecha hacia abajo              | 314    | Matrix, anticlockwise top-left              |
| 110    | Dirección de flecha, izquierda              | 315    | Matriz, esquina superior derecha a la izquierda de las agujas del reloj             |
| 111    | Gono, arriba                  | 316    | Matrix, anticlockwise bottom-right          |
| 112    | Gono, abajo                | 317    | Matrix, anticlockwise bottom-left           |
| 113    | Hexágono                       | 320    | Matriz, vertical superior izquierda, superior derecha        |
| 114    | Hexágono, girado              | 321    | Matriz, vertical inferior izquierda, inferior derecha  |
| 119    | Circle                        | 322    | Matriz, vertical superior izquierda, inferior derecha     |
| 120    | Oval, horizontal              | 323    | Matriz, vertical inferior izquierda, superior derecha     |
| 121    | Oval, vertical                | 324    | Matriz, esquina superior izquierda horizontal, inferior izquierda    |
| 122    | Ojo, horizontal               | 325    | Matriz, esquina superior derecha horizontal, inferior derecha  |
| 123    | Ojo, vertical                 | 326    | Matriz, esquina superior izquierda horizontal, inferior derecha   |
| 124    | Rectángulo redondeado, horizontal | 327    | Matriz, esquina superior derecha horizontal, parte inferior izquierda   |
| 125    | Rectángulo redondeado, vertical   | 328    | Matriz, diagonal inferior izquierda, superior derecha     |
| 127    | Estrella de 4 puntos                  | 329    | Matriz, diagonal superior izquierda, inferior derecha     |
| 128    | Estrella de 4 puntos                  | 340    | Matriz, doble matriz superior                   |
| 129    | Estrella de 6 puntos                  | 341    | Matriz, doble fondo                |
| 130    | Corazón                         | 342    | Matriz, doble matriz izquierda                  |
| 131    | Cerradura                       | 343    | Matriz, doble matriz derecha                 |
| 201    | Radial, 12 en punto            | 344    | Matriz, cuadrándular, de arriba abajo             |
| 202    | Radial, 3 en punto             | 345    | Matriz, cuadrándular, izquierda-derecha             |
| 203    | Radial, 6 en punto             | 350    | Cascada, izquierda                             |
| 204    | Radial, 9 en punto             | 351    | Cascada, derecha                            |
| 205    | Radial, 12 + 6 en punto        | 352    | Cascada, horizontal, izquierda                 |
| 206    | Radial, 3 + 9 en punto         | 353    | Cascada, horizontal, derecha                |
| 207    | Radial, 4 vías                 | 409    | Máscara aleatoria                                 |



 

 

 



