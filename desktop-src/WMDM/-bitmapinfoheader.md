---
title: Estructura de _BITMAPINFOHEADER
description: La \_ estructura BITMAPINFOHEADER define el formato de un fotograma de vídeo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Estructura _BITMAPINFOHEADER Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700181"
---
# <a name="_bitmapinfoheader-structure"></a>\_Estructura BITMAPINFOHEADER

La estructura **\_ BITMAPINFOHEADER** define el formato de un fotograma de vídeo.

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

**bisize**
</dt> <dd>

Especifica el número de bytes requerido por la estructura.

</dd> <dt>

**biwidth**
</dt> <dd>

Especifica el ancho del mapa de bits, en píxeles.

</dd> <dt>

**bialtura**
</dt> <dd>

Especifica el alto del mapa de bits, en píxeles. Si **biheight** es positivo, el mapa de bits es un DIB de nivel inferior y su origen es la esquina inferior izquierda. Si el valor de **biheight** es negativo, el mapa de bits es un DIB de arriba abajo y su origen es la esquina superior izquierda. Si el valor de **biheight** es negativo, lo que indica un DIB de arriba abajo, la **bicompresión** debe ser de BI RGB o de campos de bits de \_ BI \_ . Los DIB de arriba abajo no se pueden comprimir.

</dd> <dt>

**biplanas**
</dt> <dd>

Especifica el número de planos para el dispositivo de destino. Este valor debe establecerse en 1.

</dd> <dt>

**biBitCount**
</dt> <dd>

Especifica el número de bits por píxel. El miembro **biBitCount** de la estructura **BITMAPINFOHEADER** determina el número de bits que definen cada píxel y el número máximo de colores del mapa de bits. Este miembro debe ser uno de los valores siguientes.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | El mapa de bits es monocromo y el miembro bmiColors contiene dos entradas. Cada bit de la matriz de mapas de bits representa un píxel. Si el bit está claro, se muestra el píxel con el color de la primera entrada de la tabla bmiColors. Si se establece el bit, el píxel tiene el color de la segunda entrada de la tabla.                                                                                                                                                                                                                                                                                                        |
| 2     | El mapa de bits tiene cuatro valores de color posibles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | El mapa de bits tiene un máximo de 16 colores y el miembro bmiColors contiene hasta 16 entradas. Cada píxel del mapa de bits se representa mediante un índice de 4 bits en la tabla de colores. Por ejemplo, si el primer byte del mapa de bits es 0x1F, el byte representa dos píxeles. El primer píxel contiene el color de la segunda entrada de la tabla y el segundo píxel contiene el color de la entrada de la tabla decimosexto.                                                                                                                                                                                                                 |
| 8     | El mapa de bits tiene un máximo de 256 colores y el miembro bmiColors contiene hasta 256 entradas. En este caso, cada byte de la matriz representa un único píxel.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | El mapa de bits tiene un máximo de 2 ^ 16 colores. Si el miembro de bicompresión del BITMAPINFOHEADER es BI \_ RGB, el miembro bmiColors es **null**. Cada palabra de la matriz de mapas de bits representa un solo píxel. Las intensidades relativas de rojo, verde y azul se representan con 5 bits para cada componente de color. El valor de Blue está en los 5 bits menos significativos, seguido de 5 bits para cada verde y rojo. No se usa el bit más significativo. La tabla de colores bmiColors se usa para optimizar los colores utilizados en los dispositivos basados en paletas y debe contener el número de entradas especificadas por el miembro biClrUsed. |
| 24    | El mapa de bits tiene un máximo de 2 ^ 24 colores y el miembro bmiColors es **null**. Cada tríptico de 3 bytes de la matriz de mapas de bits representa las intensidades relativas de azul, verde y rojo, respectivamente, para un píxel. La tabla de colores bmiColors se usa para optimizar los colores utilizados en los dispositivos basados en paletas y debe contener el número de entradas especificadas por el miembro biClrUsed.                                                                                                                                                                                                                                     |
| 32    | El mapa de bits tiene un máximo de 2 ^ 32 colores. Si el miembro de bicompression es BI \_ RGB, el miembro bmiColors es **null**. Cada DWORD de la matriz de mapas de bits representa las intensidades relativas de azul, verde y rojo, respectivamente, para un píxel. No se utiliza el byte alto en cada DWORD. La tabla de colores bmiColors se usa para optimizar los colores utilizados en los dispositivos basados en paletas y debe contener el número de entradas especificadas por el miembro biClrUsed.                                                                                                                                                                 |



 

</dd> <dt>

**bicompresión**
</dt> <dd>

Especifica el tipo de compresión de un mapa de bits comprimido de arriba abajo (no se pueden comprimir los DIB de arriba abajo). Este miembro puede ser uno de los valores siguientes.



| Value         | Descripción                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RGB BI       | Formato sin comprimir.                                                                                                                                                                                                                                                                                            |
| \_campos de campos BI | Especifica que el mapa de bits no se comprime y que la tabla de colores consta de tres máscaras de color DWORD que especifican los componentes rojo, verde y azul, respectivamente, de cada píxel. Esto es válido cuando se usa con mapas de bits de 16 BPP y 32-bpp. Este valor es válido en Microsoft Windows CE versión 2,0 y versiones posteriores. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Especifica el tamaño de la imagen, en bytes. Se puede establecer en cero para los mapas de bits de BI \_ RGB.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Especifica la resolución horizontal, en píxeles por medidor, del dispositivo de destino para el mapa de bits. Una aplicación puede usar este valor para seleccionar un mapa de bits de un grupo de recursos que coincida mejor con las características del dispositivo actual.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Especifica la resolución vertical, en píxeles por medidor, del dispositivo de destino para el mapa de bits.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Especifica el número de índices de color de la tabla de colores que el mapa de bits usa realmente. Si este valor es cero, el mapa de bits utiliza el número máximo de colores correspondientes al valor del miembro **biBitCount** para el modo de compresión especificado por **bicompression**.

</dd> <dt>

**biClrImportant**
</dt> <dd>

Especifica el número de índices de color necesarios para mostrar el mapa de bits. Si este valor es cero, se requieren todos los colores.

Si biClrUsed es distinto de cero y el miembro biBitCount es menor que 16, el miembro biClrUsed especifica el número real de colores a los que accede el motor de gráficos o el controlador de dispositivo. Si biBitCount es 16 o superior, el miembro biClrUsed especifica el tamaño de la tabla de colores que se usa para optimizar el rendimiento de las paletas de colores del sistema. Si biBitCount es igual a 16 ó 32, la paleta de colores óptima se inicia inmediatamente después de las tres máscaras DWORD.

Si el mapa de bits es un mapa de bits empaquetado (un mapa de bits en el que la matriz de mapas de bits sigue inmediatamente a la \_ estructura BITMAPINFOHEADER y se hace referencia a él mediante un solo puntero), el miembro biClrUsed debe ser cero o el tamaño real de la tabla de colores.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura está contenida en una estructura **\_ VIDEOINFOHEADER** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





