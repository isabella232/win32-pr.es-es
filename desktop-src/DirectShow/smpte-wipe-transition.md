---
description: Transición de borrado de SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transición de borrado de SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47de62c450ff0d75f72e5fac466801991b987834
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537437"
---
# <a name="smpte-wipe-transition"></a>Transición de borrado de SMPTE

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La transición de borrado de SMPTE produce cualquiera de los borradores estándar definidos por la sociedad de la imagen de movimiento y los ingenieros de televisión (SMPTE) en el documento SMPTE 258M-1993, con la excepción de la división cuádruple.

![transición de borrado en curso](images/trans-wipe.png)

IDENTIFICADOR de clase (CLSID): {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

Nombre de la variable CLSID: CLSID \_ DxtJpeg

Nombre descriptivo: "DxtJpeg"

Propiedades



| Propiedad       | Tipo   | Valor predeterminado  | Descripción                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Color del borde alrededor de los bordes del patrón de barrido. El valor de este atributo es un número hexadecimal con el formato 0x *RRGGBB*, donde *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul. (Por lo tanto, rojo, verde y azul puros son 0xFF000, 0x00FF00 y 0x0000FF, respectivamente). |
| BorderSoftness | long   | 0        | Ancho de la región borrosa alrededor de los bordes del patrón de barrido. Especifique cero para ninguna región borrosa.                                                                                                                                                                                                              |
| BorderWidth    | long   | 0        | Ancho del borde sólido a lo largo de los bordes del patrón de barrido. Especifique cero para ningún borde.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Si no **es null**, especifica el nombre de un archivo JPEG que se va a usar como máscara de barrido en lugar de un borrado estándar integrado. El archivo debe contener un degradado monocromo de 8 bits por píxel. El degradado se usa como máscara para definir la progresión del barrido.                                                                 |
| MaskNum        | long   | 1        | Código de borrado de SMPTE estándar que especifica el estilo de borrado que se va a usar. Para obtener una lista de códigos de borrado y sus esquemas asociados, consulte el documento SMPTE 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Desplazamiento horizontal del origen de borrado desde el centro de la imagen. Válido solo para los valores de **MaskNum** de 101 a 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Desplazamiento Verical del origen de borrado desde el centro de la imagen. Válido solo para los valores de **MaskNum** de 101 a 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Número de veces que se va a replicar el patrón de barrido horizontalmente. Válido solo para los valores de **MaskNum** de 101 a 131.                                                                                                                                                                                                |
| Replicación     | long   | 0        | Número de veces que se va a replicar el patrón de borrado verticalmente. Válido solo para los valores de **MaskNum** de 101 a 131.                                                                                                                                                                                                  |
| ScaleX         | double | 1,0      | Cantidad por la que se va a estirar horizontalmente el borrado, como un porcentaje de la definición de borrado original. Válido solo para los valores de **MaskNum** de 101 a 131.                                                                                                                                                         |
| ScaleY         | double | 1,0      | Cantidad por la que se va a estirar verticalmente el borrado, como porcentaje de la definición de borrador original. Válido solo para los valores de **MaskNum** de 101 a 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

Esta transición admite los siguientes borradores estándar de SMPTE:



| Number | Descripción                   | Number | Descripción                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radial, izquierda a derecha, arriba                     |
| 2      | Vertical                      | 212    | Radial, arriba abajo, derecha                      |
| 3      | Superior izquierda                    | 213    | Radial, izquierda a derecha, superior inferior              |
| 4      | Esquina superior derecha                   | 214    | Radial, arriba abajo, izquierda-derecha                 |
| 5      | Inferior derecha                   | 221    | Radial, superior                                 |
| 6      | Inferior izquierda                    | 222    | Radial, derecha                               |
| 7      | Cuatro esquinas                  | 223    | Radial, inferior                              |
| 8      | Cuatro cuadrados                  | 224    | Radial, izquierda                                |
| 21     | Puertas de cortina, vertical          | 225    | Radial, en sentido de las agujas del reloj hacia abajo, hacia abajo     |
| 22     | Puertas de cortina, horizontal        | 226    | Radial, a la izquierda, en el sentido de las agujas del reloj     |
| 23     | Centro superior                    | 227    | Radial, en sentido de las agujas del reloj, en la parte inferior |
| 24     | Centro derecho                  | 228    | Radial, a la izquierda, en sentido contrario a las agujas del reloj |
| 25     | Centro inferior                 | 231    | Radial, división superior                           |
| 26     | Centro izquierdo                   | 232    | Radial, división derecha                         |
| 41     | Diagonal, NW a SE            | 233    | Radial, división inferior                        |
| 42     | Diagonal, NE a SW            | 234    | Radial, división izquierda                          |
| 43     | Triángulos, superior/inferior         | 235    | División de la parte superior radial                    |
| 44     | Triángulos, izquierda/derecha         | 236    | División radial, izquierda y derecha                    |
| 45     | Franja diagonal, SW a NE     | 241    | Esquina superior izquierda y radial                     |
| 46     | Franja diagonal, NW a SE     | 242    | Esquina inferior izquierda y radial                  |
| 47     | Cross                         | 243    | Esquina inferior derecha y radial                 |
| 48     | Cuadro de rombo                   | 244    | Esquina superior derecha y radial                    |
| 61     | Cuña, superior                    | 245    | Radial, superior izquierda, inferior derecha              |
| 62     | Cuña, derecha                  | 246    | Radial, inferior izquierda, superior derecha              |
| 63     | Cuña, inferior                 | 251    | Centrado radial, superior                          |
| 64     | Cuña, izquierda                   | 252    | Centro radial, izquierda                         |
| 65     | V                             | 253    | Centrado radial, inferior                       |
| 66     | V, derecha                      | 254    | Central radial, derecha                        |
| 67     | V, invertido                   | 261    | Radial de caja, derecha                           |
| 68     | V, izquierda                       | 262    | Radial de caja, superior                             |
| 71     | Sierra izquierda                | 263    | Centrado radial, superior, inferior                  |
| 72     | Sierra, superior                 | 264    | Centro radial, izquierda, derecha                  |
| 73     | Sierra, vertical            | 301    | Matriz, horizontal                          |
| 74     | Sierra, horizontal          | 302    | Matriz, vertical                            |
| 101    | Box                           | 303    | Matriz, diagonal, superior izquierda                  |
| 102    | Diamond                       | 304    | Matriz, diagonal, superior derecha                 |
| 103    | Triángulo, arriba                  | 305    | Matriz, diagonal, inferior derecha              |
| 104    | Triángulo, derecha               | 306    | Matriz, diagonal, inferior izquierda               |
| 105    | Triángulo, inferior              | 310    | Matriz, en la parte superior izquierda de la derecha                  |
| 106    | Triángulo, izquierda                | 311    | Matriz, hacia la derecha superior derecha                 |
| 107    | Punta de flecha, arriba                | 312    | Matriz, en el sentido de las agujas del reloj hacia la derecha              |
| 108    | Punta de flecha, derecha             | 313    | Matriz, en la parte inferior izquierda               |
| 109    | Punta de flecha, abajo              | 314    | Matriz, en la parte superior izquierda y derecha              |
| 110    | Punta de flecha, izquierda              | 315    | Matriz, en la parte superior derecha izquierda             |
| 111    | Pentágono, up                  | 316    | Matriz, en la parte inferior derecha izquierda          |
| 112    | Pentágono, abajo                | 317    | Matriz, en la parte inferior izquierda y derecha           |
| 113    | Tuerca                       | 320    | Matriz, vertical superior izquierda, superior derecha        |
| 114    | Hexágono, girado              | 321    | Matriz vertical inferior izquierda, inferior derecha  |
| 119    | Circle                        | 322    | Matriz, vertical superior izquierda, inferior derecha     |
| 120    | Oval, horizontal              | 323    | Matriz, inferior vertical izquierda, superior derecha     |
| 121    | Ovalado, vertical                | 324    | Matriz, horizontal superior izquierda, inferior izquierda    |
| 122    | Ojo, horizontal               | 325    | Matriz, horizontal superior derecha, inferior derecha  |
| 123    | Ojo, vertical                 | 326    | Matriz, horizontal superior izquierda, inferior derecha   |
| 124    | Rectángulo redondeado, horizontal | 327    | Matriz, horizontal superior derecha, inferior izquierda   |
| 125    | Rectángulo redondeado, vertical   | 328    | Matriz, inferior diagonal izquierda, superior derecha     |
| 127    | estrella de 4 puntos                  | 329    | Matriz, diagonal superior izquierda, inferior derecha     |
| 128    | estrella de 4 puntos                  | 340    | Matriz, espiral doble superior                   |
| 129    | estrella de 6 puntas                  | 341    | Matriz, doble espiral inferior                |
| 130    | Corazón                         | 342    | Matriz, doble espiral izquierda                  |
| 131    | Keyhole                       | 343    | Matriz, doble espiral derecha                 |
| 201    | Radial, 12 en punto            | 344    | Matriz, espiral cuádruple, arriba abajo             |
| 202    | Radial, 3 en punto             | 345    | Matriz, espiral cuádruple, izquierda-derecha             |
| 203    | Radial, 6 en punto             | 350    | Cascada, izquierda                             |
| 204    | Radial, 9 en punto             | 351    | Cascada, derecha                            |
| 205    | Radial, 12 + 6 en punto        | 352    | Cascada, horizontal, izquierda                 |
| 206    | Radial, 3 + 9 en punto         | 353    | Cascada, horizontal, derecha                |
| 207    | Radial, 4 vías                 | 409    | Máscara aleatoria                                 |



 

 

 



