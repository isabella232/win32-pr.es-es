---
description: Transición de clave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transición de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906445"
---
# <a name="key-transition"></a>Transición de clave

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La transición de clave realiza la creación de claves según el valor RGB, el valor alfa, el matiz o la luminancia.

La siguiente imagen muestra la transición de la clave:

![transición de clave](images/trans-key.png)

IDENTIFICADOR de clase (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}

Nombre de la variable CLSID: CLSID \_ DxtKey

Nombre descriptivo: "DxtKey"

Propiedades



| Propiedad   | Tipo  | Intervalo válido           | Descripción                                                                                                                                                                                                                                                | Se aplica a                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Matiz        | int   | de 0 a 360                 | Valor de matiz en el que se va a hacer la tecla.                                                                                                                                                                                                                             | Matiz                            |
| Invertir     | BOOL  | **False** o **true** | Valor booleano que indica si se va a invertir la operación predeterminada de la clave. Si **es false**, los píxeles de la imagen superpuestas se convierten en transparentes de la manera predeterminada. Si **es true**, la operación invierte.                                                   | Croma, matiz, luminancia, Nonred |
| KeyType    | int   | Ver comentarios           | Especifica el tipo de clave. Para obtener más información, vea la sección Comentarios.                                                                                                                                                                                              | All                            |
| Luminance  | int   | de 0 a 100                 | Valor de luminancia en el que se va a hacer la tecla.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0X0:0xFFFFFF        | Color en el que se va a hacer la tecla. El valor es un número hexadecimal con el formato 0x *RRGGBB*, donde *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul. (Rojo puro, verde y azul son 0xFF0000, 0x00FF00 y 0x0000FF, respectivamente). | Adapta                         |
| Similitud | int   | de 0 a 100                 | El intervalo de datos de color que se vuelve transparente. En los valores más altos, una mayor variedad de colores similares es transparente.                                                                                                                                        | Croma, Nonred                 |



 

## <a name="remarks"></a>Observaciones

El tipo de clave que se realiza depende del valor de la propiedad **KeyType** , que debe ser uno de los siguientes:



| Value | Enumeración       | Descripción                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Clave de croma (clave por valor RGB).                        |
| 1     | DXTKEY \_ NONRED    | Clave Nonred. (Hace que las áreas azules y verdes sean transparentes). |
| 2     | \_luminancia DXTKEY | Clave de luminancia.                                        |
| 3     | \_alfa DXTKEY     | Clave por valor alfa.                                   |
| 4     | \_matiz DXTKEY       | Clave por matiz.                                           |



 

De forma predeterminada, el tipo de clave es DXTKEY \_ Alpha.

 

 



