---
description: Define los términos que se usan en WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glosario de componentes de Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697346"
---
# <a name="windows-imaging-component-glossary"></a>Glosario de componentes de Windows Imaging

## <a name="b"></a>B

<dl> <dt>

**profundidad de bits**
</dt> <dd>

Número de valores de color que se pueden asignar a un solo píxel en una imagen. La profundidad de color puede oscilar entre 1 bit (blanco y negro) y 32 bits (más de 16,7 millones de colores). Vea también: profundidad de color

</dd> <dt>

**bits por píxel (BPP)**
</dt> <dd>

Número de bits que representan el valor de color de cada píxel de una imagen digitalizada. Vea también: BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Objeto IWICBitmapClipper.

</dd> <dt>

**Codec**
</dt> <dd>

Un filtro que comprime (codifica) o descomprime (descodifica) un flujo de datos.

</dd> <dt>

**contexto de color**
</dt> <dd>

Abstracción de un perfil de color. El perfil se puede cargar desde un archivo (es decir, "sRGB color Space Profile. ICM") o desde un búfer de memoria que se obtiene al leer. La información de contexto de color se define mediante la interfaz IWICColorContext para WIC y se recupera con el método GetColorContext.

</dd> <dt>

**transformación de color**
</dt> <dd>

Asignar colores del contexto de color de origen al contexto de color de destino en un formato de píxel de salida determinado.

</dd> <dt>

**Modelo de color CYMK**
</dt> <dd>

Espacio de colores multidimensional compuesto por las intensidades aguamarina, fucsia, amarillo y negro que constituyen un color determinado.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**descodificador**
</dt> <dd>

Véase: códec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**codificador**
</dt> <dd>

Véase: códec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**alguna**
</dt> <dd>

Un tipo de compresión que garantiza que los datos originales se pueden recuperar exactamente, sin pérdida de calidad de la imagen.

</dd> <dt>

**con pérdida**
</dt> <dd>

Se quita un proceso para comprimir los datos en los que la información no es necesaria y no se puede recuperar tras la descompresión. Normalmente se utiliza con datos de audio y objetos visuales en los que es aceptable una ligera degradación de la calidad.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**contenedor multiproceso (MTA)**
</dt> <dd>

Forma de multithreading compatible con el modelo de objetos componentes (COM). En un modelo de Apartamento multiproceso, todos los subprocesos del proceso que se han inicializado como subproceso libre se encuentran en un único apartamento.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**formato de píxel nativo**
</dt> <dd>

Uno de los formatos de píxel que proporciona WIC, donde se describe el diseño de memoria de cada píxel de un mapa de bits.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**índ**
</dt> <dd>

Conjunto de colores utilizados por un objeto o una aplicación.

</dd> <dt>

**Directiva de metadatos de fotos**
</dt> <dd>

Directiva de Windows para leer, escribir y quitar metadatos de imagen.

</dd> <dt>

**formato de píxeles**
</dt> <dd>

Tamaño y organización de los componentes de color de píxeles en la memoria. Se especifica mediante el número total de bits usados por píxel y el número de bits usados para almacenar los componentes rojo, verde, azul y alfa del color. Por ejemplo, el formato de píxel RGB24 usa 24 bits para almacenar un color de píxeles, con ocho bits cada uno para rojo, verde y azul. El formato de píxel de ARGB32 usa 32 bits, con 24 bits de información de color y 8 bits de información de canal alfa.

</dd> <dt>

**descodificación progresiva**
</dt> <dd>

Proceso para descodificar imágenes que se han codificado con información sobre los distintos niveles de descodificación.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**misiones**
</dt> <dd>

Hace referencia a una interfaz COM IStream que se puede utilizar para leer o escribir datos de forma secuencial en archivos, memoria o ubicaciones de red.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**curva de tono**
</dt> <dd>

Un gráfico que se usa en la fotografía digital y que muestra el rango tonal de la imagen.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging Component (WIC)**
</dt> <dd>

Plataforma extensible que proporciona una API de bajo nivel para imágenes digitales.

</dd> </dl>

 

 



