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
ms.openlocfilehash: dff9904eef692b3858cc044f7b400a5b3641456a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721263"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>Método IDWriteBitmapRenderTarget2:: GetBitmapData (dwrite_3. h)

Recupera los datos de píxeles de un destino de representación de mapa de bits.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, consulte [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Parámetros

`bitmapData`

Tipo: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Puntero a los datos de píxeles.

## <a name="return-value"></a>Valor devuelto

Tipo: <b>HRESULT</b>

Si este método se ejecuta correctamente, devuelve <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. De lo contrario, devuelve un código de error <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Ejemplos

Consulte el tema de [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, versión preliminar de Project reunion 0,1 [aplicaciones Win32] |
| **Header** | dwrite_3. h (incluir dwrite_core. h) |
| **Library** | Dwrite. lib |
| **DLL** | Dwrite.dll |

## <a name="see-also"></a>Vea también

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)