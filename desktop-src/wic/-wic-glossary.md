---
description: Define los términos que se usan en WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Windows Glosario de componentes de creación de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c851b4a0be5d5f90a5ff0cc030d68cc1010a0259c316811a7ca1c3b92c383b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668196"
---
# <a name="windows-imaging-component-glossary"></a>Windows Glosario de componentes de creación de imágenes

## <a name="b"></a>B

<dl> <dt>

**profundidad de bits**
</dt> <dd>

Número de valores de color que se pueden asignar a un solo píxel en una imagen. La profundidad de color puede oscilar entre 1 bit (blanco y negro) y 32 bits (más de 16,7 millones de colores). Consulte también: Profundidad de color

</dd> <dt>

**bits por píxel (bpp)**
</dt> <dd>

Número de bits que representan el valor de color de cada píxel de una imagen digitalizado. Consulte también:BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Objeto IWICBitmapClipper.

</dd> <dt>

**Codec**
</dt> <dd>

Filtro que comprime (codifica) o descomprime (descodifica) un flujo de datos.

</dd> <dt>

**contexto de color**
</dt> <dd>

Abstracción de un perfil de color. El perfil se puede cargar desde un archivo (es decir, "sRGB Color Space Profile.icm") o de un búfer de memoria obtenido mediante lectura. La interfaz IWICColorContext para WIC define la información de contexto de color y se recupera con el método GetColorContext.

</dd> <dt>

**transformación de color**
</dt> <dd>

Asignación de colores desde el contexto de color de origen al contexto de color de destino en un formato de píxel de salida determinado.

</dd> <dt>

**Modelo de color CYMK**
</dt> <dd>

Espacio de color multidimensional que consta de las intensidades multidimensionales de agua, rojo, amarillo y negro que componen un color determinado.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Decodificador**
</dt> <dd>

Consulte Otro término: códec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Codificador**
</dt> <dd>

Consulte Otro término: códec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Lossless**
</dt> <dd>

Tipo de compresión que garantiza que los datos originales se puedan recuperar exactamente, sin pérdida de calidad de imagen.

</dd> <dt>

**Lossy**
</dt> <dd>

Proceso para comprimir datos en el que se quita la información que se considera innecesaria y no se puede recuperar tras la descompresión. Normalmente se usa con datos visuales y de audio en los que una ligera degradación de la calidad es aceptable.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**apartamento multiproceso (MTA)**
</dt> <dd>

Forma de multithreading compatible con el Modelo de objetos componentes (COM). En un modelo de apartamento multiproceso, todos los subprocesos del proceso que se han inicializado como subproceso libre residen en un único apartamento.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**formato de píxel nativo**
</dt> <dd>

Uno de los formatos de píxel proporcionados por WIC, en el que se describe el diseño de memoria de cada píxel de un mapa de bits.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Paleta**
</dt> <dd>

Conjunto de colores usados por un objeto o aplicación.

</dd> <dt>

**directiva de metadatos de fotos**
</dt> <dd>

Directiva de Windows para leer, escribir y quitar metadatos de imagen.

</dd> <dt>

**formato de píxeles**
</dt> <dd>

Tamaño y organización de los componentes de color de píxel en la memoria. Se especifica por el número total de bits usados por píxel y el número de bits usados para almacenar los componentes rojo, verde, azul y alfa del color. Por ejemplo, el formato DE24 píxeles RGB usa 24 bits para almacenar un color de píxel, con ocho bits cada uno para rojo, verde y azul. El formato de píxel ARGB32 usa 32 bits, con 24 bits de información de color y 8 bits de información de canal alfa.

</dd> <dt>

**decodación progresiva**
</dt> <dd>

Proceso para descodificar imágenes que se han codificado con información sobre los distintos niveles de descodificación.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Corriente**
</dt> <dd>

Hace referencia a una interfaz COM IStream que se puede usar para leer o escribir datos secuencialmente en archivos, memoria o ubicaciones de red.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**curva de tono**
</dt> <dd>

Gráfico usado en la fotografía digital que muestra el intervalo tonal de la imagen.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging Component (WIC)**
</dt> <dd>

Una plataforma extensible que proporciona una API de bajo nivel para imágenes digitales.

</dd> </dl>

 

 



