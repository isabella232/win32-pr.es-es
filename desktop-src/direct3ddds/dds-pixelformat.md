---
title: Estructura de DDS_PIXELFORMAT (DDS. h)
description: Formato de píxel de la superficie.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- Estructura de DDS_PIXELFORMAT DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717623"
---
# <a name="dds_pixelformat-structure"></a>Estructura de PIXELFORMAT de DDS \_

Formato de píxel de la superficie.

## <a name="syntax"></a>Sintaxis


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño de la estructura; establézcalo en 32 (bytes).

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valores que indican qué tipo de datos se encuentra en la superficie.



| Marca              | Descripción                                                                                                                                                                                                                                | Value   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | La textura contiene datos alfa; **dwRGBAlphaBitMask** contiene datos válidos.                                                                                                                                                                    | 0x1     |
| \_alfa DDPF       | Se usa en algunos archivos DDS más antiguos para el canal alfa solo datos sin comprimir (dwRGBBitCount contiene el canal alfa bitCount; dwABitMask contiene datos válidos)                                                                                  | 0x2     |
| \_FourCC DDPF      | La textura contiene datos RGB comprimidos; **dwFourCC** contiene datos válidos.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | La textura contiene datos RGB sin comprimir; **dwRGBBitCount** y las máscaras RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contienen datos válidos.                                                                                           | 0x40    |
| DDPF \_ YUV         | Se usa en algunos archivos DDS más antiguos para datos YUV sin comprimir (dwRGBBitCount contiene el número de bits YUV; dwRBitMask contiene la máscara Y, dwGBitMask contiene la máscara U, dwBBitMask contiene la máscara V)                                          | 0x200   |
| \_luminancia DDPF   | Se usa en algunos archivos DDS más antiguos para los datos sin comprimir de color de canal único (dwRGBBitCount contiene el número de bits de canal de luminancia; dwRBitMask contiene la máscara de canal). Se puede combinar con DDPF \_ ALPHAPIXELS para un archivo DDS de dos canales. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Códigos de cuatro caracteres para especificar formatos comprimidos o personalizados. Los valores posibles son: *DXT1*, *DXT2*, *DXT3*, *DXT4* o *DXT5*. Un elemento FourCC de contenido DX10 indica el prescense del [**encabezado \_ DDS \_ DXT10**](dds-header-dxt10.md) el encabezado extendido y el miembro dxgiFormat de esa estructura indica el formato verdadero. Cuando se usa un código de cuatro caracteres, dwFlags debe incluir *DDPF \_ FourCC*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bits en un formato RGB (posiblemente incluido alfa). Válido cuando **dwFlags** incluye *DDPF \_ RGB*, *\_ luminancia DDPF* o *DDPF \_ YUV*.

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara roja (o lumiannce o Y) para leer los datos de color. Por ejemplo, dado el formato A8R8G8B8, la máscara roja sería 0x00ff0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara verde (o U) para leer los datos de color. Por ejemplo, dado el formato A8R8G8B8, la máscara verde sería 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara azul (o V) para leer los datos de color. Por ejemplo, dado el formato A8R8G8B8, la máscara azul sería 0x000000ff.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara alfa para leer datos alfa. dwFlags debe incluir *DDPF \_ ALPHAPIXELS* o *DDPF \_ Alpha*. Por ejemplo, dado el formato A8R8G8B8, la máscara alfa sería 0xFF000000.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para almacenar formatos de DXGI como datos de punto flotante, use un valor de **dwFlags** de DDPF \_ FourCC y establezca **dwFourCC** en ' d ', ' X ', ' 1 ', ' 0 '. Use el encabezado de extensión [**DDS \_ Header \_ DXT10**](dds-header-dxt10.md) para almacenar el formato de DXGI en el miembro **dxgiFormat** .

Tenga en cuenta que hay variantes no estándar de archivos DDS donde **dwFlags** tiene DDPF \_ FourCC y el valor **dwFourCC** se establece directamente en un valor de enumeración de formato D3DFORMAT o DXGI \_ . No es posible eliminar la ambigüedad de los valores de formato de D3DFORMAT frente a DXGI \_ mediante este esquema no estándar, por lo que se recomienda el encabezado de extensión contenido DX10 en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

