---
title: Estructura de DDS_HEADER (DDS. h)
description: Describe un encabezado de archivo DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- Estructura de DDS_HEADER DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717624"
---
# <a name="dds_header-structure"></a>\_Estructura del encabezado DDS

Describe un encabezado de archivo DDS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño de la estructura. Este miembro debe establecerse en 124.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Marcas para indicar qué miembros contienen datos válidos.



| Marca              | Descripción                                                  | Value    |
|-------------------|--------------------------------------------------------------|----------|
| \_Cap DDSD        | Se requiere en cada archivo. DDS.                                 | 0x1      |
| alto de DDSD \_      | Se requiere en cada archivo. DDS.                                 | 0x2      |
| ancho de DDSD \_       | Se requiere en cada archivo. DDS.                                 | 0x4      |
| paso de DDSD \_       | Obligatorio cuando se proporciona el tono para una textura sin comprimir. | 0x8      |
| DDSD \_ PIXELFORMAT | Se requiere en cada archivo. DDS.                                 | 0x1000   |
| DDSD \_ MIPMAPCOUNT | Obligatorio en una textura de mipmapped.                             | 0x20000  |
| DDSD \_ LINEARSIZE  | Obligatorio cuando se proporciona el tono para una textura comprimida.    | 0x80000  |
| profundidad de DDSD \_       | Obligatorio en una textura de profundidad.                                 | 0x800000 |



 

> [!Note]  
> Al escribir archivos. DDS, debe establecer las \_ marcas DDSD Caps y DDSD \_ PIXELFORMAT, y para las texturas de mipmapped, también debe establecer la marca DDSD \_ MIPMAPCOUNT. Sin embargo, cuando se lee un archivo. DDS, no se debe confiar en las \_ marcas DDSD Cap, DDSD \_ PIXELFORMAT y DDSD \_ MIPMAPCOUNT que se establecen porque es posible que algunos escritores de este tipo de archivo no establezcan estas marcas.

 

La \_ marca de \_ textura de marcas de encabezado DDS \_ , que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSD caps, DDSD \_ height, DDSD \_ width y DDSD \_ PIXELFORMAT.

La \_ \_ \_ marca de MIPMAP de marcadores de encabezado de DDS, que se define en DDS. h, es igual a la \_ marca MIPMAPCOUNT de DDSD.

La \_ \_ \_ marca de volumen de marcas de encabezado DDS, que se define en DDS. h, es igual a la \_ marca de profundidad DDSD.

La \_ \_ \_ marca de paso de marcador de encabezado DDS, que se define en DDS. h, es igual a la marca de paso de DDSD \_ .

La \_ marca LINEARSIZE de marcadores de encabezado DDS \_ \_ , que se define en DDS. h, es igual a la \_ marca LINEARSIZE de DDSD.

</dd> <dt>

**dwHeight**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Alto de superficie (en píxeles).

</dd> <dt>

**dwWidth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ancho de la superficie (en píxeles).

</dd> <dt>

**dwPitchOrLinearSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

El paso o el número de bytes por línea de examen en una textura sin comprimir; número total de bytes en la textura de nivel superior para una textura comprimida. Para obtener información sobre cómo calcular el paso, consulte la sección sobre el diseño del archivo DDS de la [Guía de programación para DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwDepth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profundidad de una textura de volumen (en píxeles), de lo contrario, sin usar.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de niveles de mipmap, de lo contrario, sin usar.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sin usar.

</dd> <dt>

**ddspf**
</dt> <dd>

Tipo: **[ **\_ PIXELFORMAT de DDS**](dds-pixelformat.md)**

</dd> <dd>

El formato de píxel (consulte las letras de la [**DDS \_**](dds-pixelformat.md)).

</dd> <dt>

**dwCaps**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Especifica la complejidad de las superficies almacenadas.



| Marca             | Descripción                                                                                                                              | Value    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| \_complejo DDSCAPS | Opta debe usarse en cualquier archivo que contenga más de una superficie (un mipmap, un mapa de entorno cúbico o una textura de volumen mipmapped). | 0x8      |
| \_MIPMAP DDSCAPS  | Opta debe utilizarse para un mipmap.                                                                                                   | 0x400000 |
| \_textura DDSCAPS | Obligatorio                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Al escribir archivos. DDS, debe establecer la \_ marca de textura DDSCAPS y, en el caso de varias superficies, también debe establecer la \_ marca DDSCAPS Complex. Sin embargo, al leer un archivo. DDS, no debe confiar en las marcas DDSCAPS \_ Texture y DDSCAPS \_ Complex que se establecen porque algunos escritores de este tipo de archivo podrían no establecer estas marcas.

 

La \_ marca del mipmap de marcas de la superficie DDS \_ \_ , que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas de mipmap complejo y DDSCAPS de DDSCAPS \_ .

La \_ \_ \_ marca de textura de las marcas de la superficie DDS, que se define en DDS. h, es igual a la \_ marca de textura DDSCAPS.

La \_ marca DDS Surface \_ Flags \_ mapa, que se define en DDS. h, es igual a la \_ marca compleja DDSCAPS.

</dd> <dt>

**dwCaps2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Detalles adicionales sobre las superficies almacenadas.



| Marca                         | Descripción                                            | Value    |
|------------------------------|--------------------------------------------------------|----------|
| DDSCAPS2 \_ mapa            | Obligatorio para un mapa de cubo.                               | 0x200    |
| DDSCAPS2 \_ mapa \_ POSITIVEX | Obligatorio cuando estas superficies están almacenadas en un mapa de cubo. | 0x400    |
| DDSCAPS2 \_ mapa \_ NEGATIVEX | Obligatorio cuando estas superficies están almacenadas en un mapa de cubo. | 0x800    |
| DDSCAPS2 \_ mapa \_ positivo | Obligatorio cuando estas superficies están almacenadas en un mapa de cubo. | 0x1000   |
| DDSCAPS2 \_ mapa \_ negativo | Obligatorio cuando estas superficies están almacenadas en un mapa de cubo. | 0x2000   |
| DDSCAPS2 \_ mapa \_ POSITIVEZ | Obligatorio cuando estas superficies están almacenadas en un mapa de cubo. | 0x4000   |
| DDSCAPS2 \_ mapa \_ NEGATIVEZ | Obligatorio cuando estas superficies están almacenadas en un mapa de cubo. | 0x8000   |
| \_Volumen DDSCAPS2             | Obligatorio para una textura de volumen.                         | 0x200000 |



 

La \_ marca DDS mapa \_ POSITIVEX, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa POSITIVEX \_ \_ .

La \_ marca DDS mapa \_ NEGATIVEX, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa NEGATIVEX \_ \_ .

La \_ marca DDS mapa \_ positivo, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas mapa DDSCAPS2 y DDSCAPS2 \_ mapa \_ .

La \_ marca DDS mapa \_ Negative, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 \_ mapa \_ .

La \_ marca DDS mapa \_ POSITIVEZ, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa POSITIVEZ \_ \_ .

La \_ marca DDS mapa \_ NEGATIVEZ, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa NEGATIVEZ \_ \_ .

La \_ marca DDS mapa \_ ALLFACES, que se define en DDS. h, es una combinación bit a bit de las \_ marcas DDS mapa \_ POSITIVEX, DDS \_ mapa \_ NEGATIVEX, DDS \_ mapa \_ positivo, DDS \_ mapa \_ negativo, DDS \_ mapa \_ POSITIVEZ y \_ \_ DDSCAPS2 mapa NEGATIVEZ.

La \_ marca de volumen de marcas DDS \_ , que se define en DDS. h, es igual a la \_ marca de volumen DDSCAPS2.

> [!Note]  
> Aunque Direct3D 9 admite mapas de cubos parciales, Direct3D 10, 10,1 y 11 requieren que se definan las seis caras del mapa de cubos (es decir, se debe establecer DDS \_ mapa \_ ALLFACES).

 

</dd> <dt>

**dwCaps3**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sin usar.

</dd> <dt>

**dwCaps4**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sin usar.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sin usar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Incluir marcas en **dwFlags** para los miembros de la estructura que contienen datos válidos.

Use esta estructura en combinación con un [**\_ encabezado DDS \_ DXT10**](dds-header-dxt10.md) para almacenar una matriz de recursos en un archivo DDS. Para obtener más información, consulte [matrices de texturas](dx-graphics-dds-pguide.md).

**DDS \_ El encabezado** es idéntico a la estructura DDSURFACEDESC2 de DirectDraw sin dependencias de DirectDraw.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

