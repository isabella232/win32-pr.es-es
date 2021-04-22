---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Crea un objeto de generador que se usa para la creación posterior de objetos DWriteCore individuales.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882146"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>Función DWriteCoreCreateFactory (dwrite_core.h)

Crea un objeto de generador que se usa para la creación posterior de objetos DWriteCore individuales.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore [de DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)

## <a name="syntax"></a>Sintaxis
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>Parámetros

`factoryType`

Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

Valor que especifica si el objeto de generador se compartirá, aislará o restringirá.

`iid`

Tipo: <b>REFIID</b>

Valor GUID que identifica la interfaz del generador de DirectWrite, como __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).

`factory`

Tipo: <b>IUnknown**</b>

Dirección de un puntero al objeto de generador directWrite recién creado.

## <a name="return-value"></a>Valor devuelto

Tipo: <b>HRESULT</b>

Si este método se realiza correctamente, devuelve <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. De lo contrario, devuelve un código de error <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT.</b>

## <a name="examples"></a>Ejemplos

Consulte el tema [de información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Observaciones

Esto es funcionalmente igual que la función [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada por la versión del sistema de DirectWrite. La función DWriteCore tiene un nombre diferente para evitar ambigüedades.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, Project Project Project [Aplicaciones Win32] |
| **Header** | dwrite.h (incluir dwrite_core.h) |
