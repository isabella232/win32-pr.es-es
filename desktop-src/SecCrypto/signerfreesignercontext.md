---
description: Libera una estructura SIGNER \_ CONTEXT asignada por una llamada anterior a la función SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: Función SignerFreeSignerContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8338e346db49b21f9eccfca11a7e1a1fff0c42f0a013139a097385fbbe90c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973196"
---
# <a name="signerfreesignercontext-function"></a>Función SignerFreeSignerContext

La **función SignerFreeSignerContext** libera una estructura [**\_ SIGNER CONTEXT**](signer-context.md) asignada por una llamada anterior a la función [**SignerSignEx.**](signersignex.md)

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSignerContext* \[ En\]
</dt> <dd>

Puntero a la estructura [**SIGNER \_ CONTEXT**](signer-context.md) que se liberará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CONTEXTO DEL \_ FIRMANTE**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
