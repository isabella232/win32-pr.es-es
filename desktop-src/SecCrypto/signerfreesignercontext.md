---
description: Libera una estructura de contexto de firmante \_ asignada por una llamada anterior a la función SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext función)
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
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667905"
---
# <a name="signerfreesignercontext-function"></a>SignerFreeSignerContext función)

La función **SignerFreeSignerContext** libera una estructura de [**\_ contexto de firmante**](signer-context.md) asignada por una llamada anterior a la función [**SignerSignEx**](signersignex.md) .

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSignerContext* \[ de\]
</dt> <dd>

Puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**contexto del firmante \_**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
