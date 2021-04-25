---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que se puede usar para representar glifos.
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
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
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
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: 482aff4e2b9fbf03a89a15a7e38cc07d7542362b
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955038"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>Interfaz IDWriteBitmapRenderTarget2 (dwrite_3.h)

Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que se puede usar para representar glifos.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](/windows/win32/directwrite/dwritecore-overview)

## <a name="inheritance"></a>Herencia

La **interfaz IDWriteBitmapRenderTarget2** hereda de [IDWriteBitmapRenderTarget1.](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)

## <a name="methods"></a>Métodos

La **interfaz IDWriteBitmapRenderTarget2** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2::GetBitmapData](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | Recupera los datos de píxeles de un destino de representación de mapa de bits. |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, Project Project Project [Aplicaciones Win32] |
| **Header** | dwrite_3.h (incluir dwrite_core.h) |
