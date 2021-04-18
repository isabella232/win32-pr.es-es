---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Representa los datos de mapa de bits en formato BGRA32.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: ea60bbd4933cd890321e0caeb095778922699a46
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721261"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>Estructura de DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)

Representa los datos de mapa de bits en formato BGRA32.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, consulte [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Sintaxis

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>Miembros

`width`

Tipo: **[UINT32](../../winprog/windows-data-types.md)**

Ancho, en píxeles, del mapa de bits.


`height`

Tipo: **[UINT32](../../winprog/windows-data-types.md)**

Alto, en píxeles, del mapa de bits.


`pixels`

Tipo: \_ \_ tamaño \_ del campo (ancho * alto)**[UINT32](../../winprog/windows-data-types.md)\***

Puntero a la ubicación de los valores de bit del mapa de bits.


## <a name="examples"></a>Ejemplos

Consulte el tema de [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, versión preliminar de Project reunion 0,1 [aplicaciones Win32] |
| **Header** | dwrite_3. h (incluir dwrite_core. h) |