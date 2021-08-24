---
UID: ''
title: Función UnicodeToBytes
description: Convierte caracteres Unicode en bytes GB18030.
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
ms.openlocfilehash: 01109763644dc04aeb398e5fc64e221cd5f3d18870df2654fa5348bc163a277c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764743"
---
# <a name="unicodetobytes-function"></a>Función UnicodeToBytes

## <a name="description"></a>Descripción

En desuso. Convierte caracteres Unicode en bytes GB18030.

**Nota**  Al convertir caracteres Unicode en bytes GB18030, una aplicación para ejecutarse en Windows Vista y versiones posteriores debe usar la función [WideCharToMultiByte.](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

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

Puntero a la cadena Unicode que se convertirá.

### <a name="cchwidechar-in"></a>cchWideChar [in]

Recuento de caracteres de la cadena Unicode que se convertirá.

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

Puntero al búfer multibyte de destino.
Si *lpMultiByteStr* es 0, se devuelve el recuento de bytes del resultado GB18030 y no se realiza ninguna conversión.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Recuento de bytes del búfer multibyte de destino.
Si *cchMultiByte* es 0, se devuelve el recuento de bytes del resultado GB18030 y no se realiza ninguna conversión.

## <a name="returns"></a>Devoluciones

Devuelve el recuento de bytes de los caracteres multibyte que se generan, si se realiza correctamente.

## <a name="remarks"></a>Comentarios

## <a name="see-also"></a>Vea también

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
