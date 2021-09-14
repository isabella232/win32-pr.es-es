---
description: Transición de claves
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transición de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061044"
---
# <a name="key-transition"></a>Transición de claves

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La transición de clave realiza la clave en función del valor RGB, el valor alfa, el matiz o la luminosidad.

En la imagen siguiente se muestra la transición de clave:

![transición de claves](images/trans-key.png)

Id. de clase (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}

Nombre de variable CLSID: CLSID \_ DxtKey

Nombre descriptivo: "DxtKey"

Propiedades



| Propiedad   | Tipo  | Intervalo válido           | Descripción                                                                                                                                                                                                                                                | Se aplica a                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Matiz        | int   | 0–360                 | Valor de matiz en el que se va a claver.                                                                                                                                                                                                                             | Matiz                            |
| Invertir     | BOOL  | **FALSE** o **TRUE** | Valor booleano que indica si se debe invertir la operación predeterminada de la clave. Si **es FALSE,** los píxeles de la imagen de sobresaliendo se hacen transparentes de la manera predeterminada. Si **es TRUE,** la operación invierte.                                                   | Ance, Hue, Luminance, Nonred |
| KeyType    | int   | Consulte Comentarios.           | Especifica el tipo de clave. Para obtener más información, vea la sección Comentarios.                                                                                                                                                                                              | All                            |
| Luminance  | int   | 0–100                 | Valor de luminosidad en el que se va a claver.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0x0: 0xFFFFFF        | Color en el que se va a claver. El valor es un número hexadecimal con el formato 0x *RRGGBB*, donde *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul. (Rojo puro, verde y azul son 0xFF0000, 0x00FF00 y 0x0000FF, respectivamente). | Chroma                         |
| Similitud | int   | 0–100                 | Intervalo de datos de color que se vuelve transparente. En valores más altos, una gama más amplia de colores similares es transparente.                                                                                                                                        | Verón, nored                 |



 

## <a name="remarks"></a>Observaciones

El tipo de clave que se realiza depende del valor de la **propiedad KeyType,** que debe ser una de las siguientes:



| Value | Enumeración       | Descripción                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Tecla de descifrado (clave por valor RGB).                        |
| 1     | DXTKEY \_ NONRED    | Clave nored. (Hace que las áreas azul y verde sea transparente). |
| 2     | DXTKEY \_ LUMINANCE | Tecla de luminosidad.                                        |
| 3     | DXTKEY \_ ALPHA     | Clave por valor alfa.                                   |
| 4     | DXTKEY \_ HUE       | Clave por matiz.                                           |



 

El tipo de clave tiene como valor predeterminado DXTKEY \_ ALPHA.

 

 



