---
UID: ''
title: UnicodeToBytes función)
description: Convierte los caracteres Unicode a GB18030 bytes.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "103785489"
---
# <a name="unicodetobytes-function"></a>UnicodeToBytes función)

## <a name="description"></a>Descripción

En desuso. Convierte los caracteres Unicode a GB18030 bytes.

**Nota:**  Al convertir los caracteres Unicode a GB18030 bytes, una aplicación que se ejecute en Windows Vista y versiones posteriores debería usar la función [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Parámetros

### <a name="lpwidecharstr-in"></a>lpWideCharStr [in]

Puntero a la cadena Unicode que se va a convertir.

### <a name="cchwidechar-in"></a>cchWideChar [in]

Recuento de caracteres de la cadena Unicode que se va a convertir.

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

Puntero al búfer multibyte de destino.
Si *lpMultiByteStr* es 0, se devuelve el recuento de bytes del resultado de GB18030 y no se realiza ninguna conversión.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Recuento de bytes del búfer multibyte de destino.
Si *cchMultiByte* es 0, se devuelve el recuento de bytes del resultado de GB18030 y no se realiza ninguna conversión.

## <a name="returns"></a>Devoluciones

Devuelve el recuento de bytes de los caracteres multibyte que se generan si se realiza correctamente.

## <a name="remarks"></a>Observaciones

## <a name="see-also"></a>Vea también

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
