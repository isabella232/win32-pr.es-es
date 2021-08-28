---
title: DDS_PIXELFORMAT estructura (Dds.h)
description: Formato de píxeles de superficie.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT DDS de estructura
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
ms.openlocfilehash: 08e2c8d4b5e30a3a5a9a039e27f5704019a6300c
ms.sourcegitcommit: 205567a2a76ad672a493a0203ff9d61271d9df98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/18/2021
ms.locfileid: "122358911"
---
# <a name="dds_pixelformat-structure"></a>Estructura PIXELFORMAT de DDS \_

Formato de píxeles de superficie.

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

Tamaño de la estructura; se establece en 32 (bytes).

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valores que indican qué tipo de datos hay en la superficie.



| Marca              | Descripción                                                                                                                                                                                                                                | Valor   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | La textura contiene datos alfa; **dwRGBAlphaBitMask contiene** datos válidos.                                                                                                                                                                    | 0x1     |
| DDPF \_ ALPHA       | Se usa en algunos archivos DDS anteriores solo para datos sin comprimir del canal alfa (dwRGBBitCount contiene el recuento de bits del canal alfa; dwABitMask contiene datos válidos)                                                                                  | 0x2     |
| DDPF \_ FOURCC      | La textura contiene datos RGB comprimidos; **dwFourCC contiene** datos válidos.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | La textura contiene datos RGB sin comprimir; **dwRGBBitCount y** las máscaras RGB **(dwRBitMask,** **dwGBitMask,** **dwBBitMask)** contienen datos válidos.                                                                                           | 0x40    |
| DDPF \_ YUV         | Se usa en algunos archivos DDS anteriores para datos sin comprimir de YUV (dwRGBBitCount contiene el recuento de bits YUV; dwRBitMask contiene la máscara Y, dwGBitMask contiene la máscara U, dwBBitMask contiene la máscara V)                                          | 0x200   |
| DDPF \_ LUMINANCE   | Se usa en algunos archivos DDS anteriores para datos sin comprimir de color de canal único (dwRGBBitCount contiene el recuento de bits del canal de luminosidad; dwRBitMask contiene la máscara del canal). Se puede combinar con DDPF \_ ALPHAPIXELS para un archivo DDS de dos canales. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Códigos de cuatro caracteres para especificar formatos comprimidos o personalizados. Los valores posibles *son: DXT1,* *DXT2,* *DXT3,* *DXT4* o *DXT5.* Un FourCC de DX10 indica el prescense del encabezado extendido [**\_ \_ DDS HEADER DXT10**](dds-header-dxt10.md) y el miembro dxgiFormat de esa estructura indica el formato verdadero. Cuando se usa un código de cuatro caracteres, dwFlags debe incluir *DDPF \_ FOURCC*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bits en un formato RGB (posiblemente incluido alfa). Válido cuando **dwFlags** incluye *DDPF \_ RGB,* *DDPF \_ LUMINANCE* o *DDPF \_ YUV.*

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara roja (o de luminosidad o Y) para leer datos de color. Por ejemplo, dado el formato A8R8G8B8, la máscara roja se 0x00ff0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara verde (o U) para leer datos de color. Por ejemplo, dado el formato A8R8G8B8, la máscara verde se 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara azul (o V) para leer datos de color. Por ejemplo, dado el formato A8R8G8B8, la máscara azul se 0x000000ff.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara alfa para leer datos alfa. dwFlags debe incluir *DDPF \_ ALPHAPIXELS* o *DDPF \_ ALPHA.* Por ejemplo, dado el formato A8R8G8B8, la máscara alfa se 0xff000000.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para almacenar formatos DXGI como datos de punto flotante, use **dwFlags** de DDPF FOURCC y establezca \_ **dwFourCC** en "D", "X", "1", "0". Use el [**encabezado de extensión DDS \_ HEADER \_ DXT10**](dds-header-dxt10.md) para almacenar el formato DXGI en el **miembro dxgiFormat.**

Tenga en cuenta que hay variantes no estándar de archivos DDS donde **dwFlags** tiene DDPF FOURCC y el valor dwFourCC se establece directamente en un valor de enumeración \_ D3DFORMAT o DXGI  \_ FORMAT. No es posible eliminar la ambigüedad de los valores D3DFORMAT frente a DXGI FORMAT mediante este esquema no estándar, por lo que se recomienda el encabezado de extensión \_ DX10 en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

