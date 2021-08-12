---
title: _BITMAPINFOHEADER estructura
description: La \_ estructura BITMAPINFOHEADER define el formato de un fotograma de vídeo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER estructura windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2d0da3d05fe050f32d5a35bbbe7de558e1c4962fa84a958855b2960e343942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586889"
---
# <a name="_bitmapinfoheader-structure"></a>\_BITMAPINFOHEADER (estructura)

La **\_ estructura BITMAPINFOHEADER** define el formato de un fotograma de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**biSize**
</dt> <dd>

Especifica el número de bytes requeridos por la estructura .

</dd> <dt>

**biWidth**
</dt> <dd>

Especifica el ancho del mapa de bits, en píxeles.

</dd> <dt>

**biHeight**
</dt> <dd>

Especifica el alto del mapa de bits, en píxeles. Si **biHeight es** positivo, el mapa de bits es un DIB de abajo arriba y su origen es la esquina inferior izquierda. Si **biHeight es** negativo, el mapa de bits es un DIB de arriba abajo y su origen es la esquina superior izquierda. Si **biHeight** es negativo, lo que indica un DIB de arriba a abajo, **biCompression** debe ser BI RGB o \_ BI \_ BITFIELDS. Las DIB de arriba abajo no se pueden comprimir.

</dd> <dt>

**Biplanos**
</dt> <dd>

Especifica el número de planos para el dispositivo de destino. Este valor debe establecerse en 1.

</dd> <dt>

**biBitCount**
</dt> <dd>

Especifica el número de bits por píxel. El **miembro biBitCount** de la estructura **BITMAPINFOHEADER** determina el número de bits que definen cada píxel y el número máximo de colores del mapa de bits. Este miembro debe ser uno de los siguientes valores.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | El mapa de bits es monocromático y el miembro bmiColors contiene dos entradas. Cada bit de la matriz de mapa de bits representa un píxel. Si el bit está claro, el píxel se muestra con el color de la primera entrada de la tabla bmiColors; si se establece el bit, el píxel tiene el color de la segunda entrada de la tabla.                                                                                                                                                                                                                                                                                                        |
| 2     | El mapa de bits tiene cuatro valores de color posibles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | El mapa de bits tiene un máximo de 16 colores y el miembro bmiColors contiene hasta 16 entradas. Cada píxel del mapa de bits se representa mediante un índice de 4 bits en la tabla de colores. Por ejemplo, si el primer byte del mapa de bits 0x1F, el byte representa dos píxeles. El primer píxel contiene el color de la segunda entrada de tabla y el segundo píxel contiene el color de la decimosexta entrada de tabla.                                                                                                                                                                                                                 |
| 8     | El mapa de bits tiene un máximo de 256 colores y el miembro bmiColors contiene hasta 256 entradas. En este caso, cada byte de la matriz representa un solo píxel.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | El mapa de bits tiene un máximo de 2^16 colores. Si el miembro biCompression de BITMAPINFOHEADER es BI \_ RGB, el miembro bmiColors es **NULL.** Cada WORD de la matriz de mapa de bits representa un solo píxel. Las intensidades relativas de rojo, verde y azul se representan con 5 bits para cada componente de color. El valor de azul está en los 5 bits menos significativos, seguido de 5 bits cada uno para verde y rojo. No se usa el bit más significativo. La tabla de colores bmiColors se usa para optimizar los colores usados en dispositivos basados en paleta y debe contener el número de entradas especificadas por el miembro biClrUsed. |
| 24    | El mapa de bits tiene un máximo de 2^24 colores y el miembro bmiColors es **NULL.** Cada triplete de 3 bytes de la matriz de mapas de bits representa las intensidades relativas de azul, verde y rojo, respectivamente, para un píxel. La tabla de colores bmiColors se usa para optimizar los colores usados en dispositivos basados en paleta y debe contener el número de entradas especificadas por el miembro biClrUsed.                                                                                                                                                                                                                                     |
| 32    | El mapa de bits tiene un máximo de 2^32 colores. Si el miembro biCompression es BI \_ RGB, el miembro bmiColors es **NULL.** Cada DWORD de la matriz de mapas de bits representa las intensidades relativas de azul, verde y rojo, respectivamente, para un píxel. No se usa el byte alto de cada DWORD. La tabla de colores bmiColors se usa para optimizar los colores usados en dispositivos basados en paleta y debe contener el número de entradas especificadas por el miembro biClrUsed.                                                                                                                                                                 |



 

</dd> <dt>

**biCompression**
</dt> <dd>

Especifica el tipo de compresión para un mapa de bits de abajo arriba comprimido (las DIB de arriba abajo no se pueden comprimir). Este miembro puede ser uno de los siguientes valores.



| Value         | Descripción                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BI \_ RGB       | Formato sin comprimir.                                                                                                                                                                                                                                                                                            |
| CAMPOS DE BITS DE BI \_ | Especifica que el mapa de bits no está comprimido y que la tabla de colores consta de tres máscaras de color DWORD que especifican los componentes rojo, verde y azul, respectivamente, de cada píxel. Esto es válido cuando se usa con mapas de bits de 16 bpp y 32 bpp. Este valor es válido en Microsoft Windows CE versión 2.0 y posteriores. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Especifica el tamaño de la imagen, en bytes. Esto se puede establecer en cero para los mapas de \_ bits RGB de BI.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Especifica la resolución horizontal, en píxeles por medidor, del dispositivo de destino para el mapa de bits. Una aplicación puede usar este valor para seleccionar un mapa de bits de un grupo de recursos que mejor coincida con las características del dispositivo actual.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Especifica la resolución vertical, en píxeles por medidor, del dispositivo de destino para el mapa de bits.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Especifica el número de índices de color de la tabla de colores que usa realmente el mapa de bits. Si este valor es cero, el mapa de bits usa el número máximo de colores correspondiente al valor del **miembro biBitCount** para el modo de compresión especificado por **biCompression**.

</dd> <dt>

**biClrImportant**
</dt> <dd>

Especifica el número de índices de color necesarios para mostrar el mapa de bits. Si este valor es cero, se requieren todos los colores.

Si biClrUsed es distinto de cero y el miembro biBitCount es menor que 16, el miembro biClrUsed especifica el número real de colores a los que accede el motor gráfico o el controlador del dispositivo. Si biBitCount es 16 o superior, el miembro biClrUsed especifica el tamaño de la tabla de colores utilizada para optimizar el rendimiento de las paletas de colores del sistema. Si biBitCount es igual a 16 o 32, la paleta de colores óptima comienza inmediatamente después de las tres máscaras DWORD.

Si el mapa de bits es un mapa de bits empaquetado (un mapa de bits en el que la matriz de mapas de bits sigue inmediatamente la estructura BITMAPINFOHEADER y se hace referencia a él mediante un solo puntero), el miembro biClrUsed debe ser cero o el tamaño real de la tabla de \_ colores.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se encuentra dentro de una **\_ estructura VIDEOINFOHEADER.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





