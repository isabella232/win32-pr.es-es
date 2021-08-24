---
title: DDS_HEADER estructura (Dds.h)
description: Describe un encabezado de archivo DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER DDS de estructura
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
ms.openlocfilehash: d974c319206d0a0cbe6abda291e9d376bd6478a5b8eb8ba3ef3bb12f182b1288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746005"
---
# <a name="dds_header-structure"></a>Estructura DE ENCABEZADO de DDS \_

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
| LÍMITES de DDSD \_        | Obligatorio en cada archivo .dds.                                 | 0x1      |
| DDSD \_ HEIGHT      | Obligatorio en cada archivo .dds.                                 | 0x2      |
| DDSD \_ WIDTH       | Obligatorio en cada archivo .dds.                                 | 0x4      |
| DDSD \_ PITCH       | Se requiere cuando se proporciona el tono para una textura sin comprimir. | 0x8      |
| DDSD \_ PIXELFORMAT | Obligatorio en cada archivo .dds.                                 | 0x1000   |
| MIPMAPCOUNT de DDSD \_ | Obligatorio en una textura mipmapped.                             | 0x20000  |
| DDSD \_ LINEARSIZE  | Se requiere cuando se proporciona el tono para una textura comprimida.    | 0x80000  |
| PROFUNDIDAD DE \_ DDSD       | Requerido en una textura de profundidad.                                 | 0x800000 |



 

> [!Note]  
> Al escribir archivos .dds, debe establecer las marcas DDSD CAPS y DDSD PIXELFORMAT y, para las texturas mipmapped, también debe establecer la marca \_ \_ \_ MIPMAPCOUNT de DDSD. Sin embargo, al leer un archivo .dds, no debe confiar en las marcas DDSD \_ CAPS, DDSD PIXELFORMAT y \_ DDSD MIPMAPCOUNT que se establecen porque algunos escritores de este tipo de archivo podrían no establecer estas \_ marcas.

 

La marca TEXTURE de DDS HEADER FLAGS, que se define en Dds.h, es una combinación or bit a bit de las marcas \_ \_ \_ DDSD \_ CAPS, DDSD \_ HEIGHT, DDSD WIDTH y \_ DDSD \_ PIXELFORMAT.

La marca MIPMAP DE DDS HEADER FLAGS, que se define en Dds.h, es igual a la marca \_ \_ \_ \_ MIPMAPCOUNT de DDSD.

La marca DE VOLUMEN DDS HEADER FLAGS, que se define en Dds.h, es igual a la marca DEPTH de \_ \_ \_ DDSD. \_

La marca PITCH de DDS HEADER FLAGS, que se define en Dds.h, es igual a la marca PITCH de \_ \_ \_ DDSD. \_

La marca DDS HEADER FLAGS LINEARSIZE, que se define en Dds.h, es igual a la marca LINEARSIZE de \_ \_ \_ DDSD. \_

</dd> <dt>

**dwHeight**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Alto de la superficie (en píxeles).

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

El tono o el número de bytes por línea de examen en una textura sin comprimir; el número total de bytes de la textura de nivel superior para una textura comprimida. Para obtener información sobre cómo calcular el tono, vea la sección Diseño de archivos DDS de la Guía de [programación para DDS.](dx-graphics-dds-pguide.md)

</dd> <dt>

**dwDepth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profundidad de una textura de volumen (en píxeles), en caso contrario, sin usar.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de niveles de mapa mip; de lo contrario, no se usa.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sin usar.

</dd> <dt>

**ddspf**
</dt> <dd>

Tipo: **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**

</dd> <dd>

El formato de píxel (vea [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).

</dd> <dt>

**dwCaps**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Especifica la complejidad de las superficies almacenadas.



| Marca             | Descripción                                                                                                                              | Value    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| DDSCAPS \_ COMPLEX | Opcional; debe usarse en cualquier archivo que contenga más de una superficie (un mapa mipmap, un mapa de entorno cúbica o una textura de volumen mipmapped). | 0x8      |
| MIPMAP de DDSCAPS \_  | Opcional; debe usarse para un mapa mip.                                                                                                   | 0x400000 |
| TEXTURA DDSCAPS \_ | Requerido                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Al escribir archivos .dds, debe establecer la marca TEXTURE de DDSCAPS Y, para varias superficies, también debe establecer la marca \_ COMPLEX de DDSCAPS. \_ Sin embargo, al leer un archivo .dds, no debe confiar en las marcas TEXTURE y \_ DDSCAPS COMPLEX de DDSCAPS que se establecen porque es posible que algunos escritores de este tipo de archivo no establezcan estas \_ marcas.

 

La marca MIPMAP DDS SURFACE FLAGS, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ \_ \_ MIPMAP DDSCAPS COMPLEX y DDSCAPS. \_

La marca TEXTURE de DDS SURFACE FLAGS, que se define en Dds.h, es igual a la marca \_ \_ TEXTURE de \_ DDSCAPS. \_

La marca CUBEMAP de DDS SURFACE FLAGS, que se define en Dds.h, es igual a la marca \_ \_ COMPLEX de \_ DDSCAPS. \_

</dd> <dt>

**dwCaps2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Detalles adicionales sobre las superficies almacenadas.



| Marca                         | Descripción                                            | Value    |
|------------------------------|--------------------------------------------------------|----------|
| MAPA DE CUBO DE DDSCAPS2 \_            | Necesario para un mapa de cubo.                               | 0x200    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEX | Se requiere cuando estas superficies se almacenan en un mapa de cubo. | 0x400    |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX | Se requiere cuando estas superficies se almacenan en un mapa de cubo. | 0x800    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEY | Se requiere cuando estas superficies se almacenan en un mapa de cubo. | 0x1000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEY | Se requiere cuando estas superficies se almacenan en un mapa de cubo. | 0x2000   |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ | Se requiere cuando estas superficies se almacenan en un mapa de cubo. | 0x4000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ | Se requiere cuando estas superficies se almacenan en un mapa de cubo. | 0x8000   |
| VOLUMEN DDSCAPS2 \_             | Necesario para una textura de volumen.                         | 0x200000 |



 

La marca DDS CUBEMAP POSITIVEX, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ DDSCAPS2 CUBEMAP y \_ DDSCAPS2 \_ CUBEMAP \_ POSITIVEX.

La marca DDS CUBEMAP NEGATIVEX, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ DDSCAPS2 CUBEMAP y \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX.

La marca DDS CUBEMAP POSITIVEY, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ DDSCAPS2 CUBEMAP y \_ DDSCAPS2 \_ CUBEMAP \_ POSITIVEY.

La marca DDS CUBEMAP NEGATIVEY, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ DDSCAPS2 CUBEMAP y \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEY.

La marca DDS CUBEMAP POSITIVEZ, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ DDSCAPS2 CUBEMAP y \_ DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ.

La marca DDS CUBEMAP NEGATIVEZ, que se define en Dds.h, es una combinación OR bit a bit de las marcas \_ \_ DDSCAPS2 CUBEMAP y \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ.

La marca DDS CUBEMAP ALLFACES, que se define en Dds.h, es una combinación or bit a bit de las marcas \_ \_ \_ DDS CUBEMAP \_ POSITIVEX, DDS \_ CUBEMAP \_ NEGATIVEX, DDS \_ CUBEMAP \_ POSITIVEY, DDS \_ CUBEMAP \_ NEGATIVEY, DDS \_ CUBEMAP POSITIVEZ y \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ.

La marca DDS FLAGS VOLUME, que se define en Dds.h, es igual a la marca \_ \_ VOLUME de DDSCAPS2. \_

> [!Note]  
> Aunque Direct3D 9 admite mapas de cubo parciales, Direct3D 10, 10.1 y 11 requieren que defina las seis caras de mapa de cubo (es decir, debe establecer DDS \_ CUBEMAP \_ ALLFACES).

 

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

## <a name="remarks"></a>Comentarios

Incluya marcas en **dwFlags para** los miembros de la estructura que contienen datos válidos.

Use esta estructura en combinación con [**un DDS \_ HEADER \_ DXT10**](dds-header-dxt10.md) para almacenar una matriz de recursos en un archivo DDS. Para obtener más información, vea [matrices de textura.](dx-graphics-dds-pguide.md)

**DDS \_ HEADER** es idéntico a la estructura DDSURFACEDESC2 de DirectDraw sin dependencias de DirectDraw.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

