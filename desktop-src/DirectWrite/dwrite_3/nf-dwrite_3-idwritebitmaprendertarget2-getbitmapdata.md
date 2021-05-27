---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Recupera los datos de píxeles de un destino de representación de mapa de bits.
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550290"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>Método IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)

Recupera los datos de píxeles de un destino de representación de mapa de bits.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore [de DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](../dwritecore-overview.md)

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Parámetros

`bitmapData`

Tipo: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Puntero a los datos de píxel.

## <a name="return-value"></a>Valor devuelto

Tipo: <b>HRESULT</b>

Si este método se realiza correctamente, devuelve <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. De lo contrario, devuelve un código de error <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT.</b>

## <a name="examples"></a>Ejemplos

Consulte el tema [de información general de DWriteCore](../dwritecore-overview.md) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, Project Project Project [Aplicaciones Win32] |
| **Header** | dwrite_3.h (incluir dwrite_core.h) |
| **Library** | Dwrite.lib |
| **Dll** | Dwrite.dll |

## <a name="see-also"></a>Consulte también

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)