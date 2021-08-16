---
description: Compara dos tokens de acceso y determina si son equivalentes con respecto a una llamada a la función AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Función NtCompareTokens (Ntseapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: a763f6f4238632c3bcc736ebacbd2ff133b1955da673a0397ba9a95ebb87c2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780567"
---
# <a name="ntcomparetokens-function"></a>Función NtCompareTokens

La **función NtCompareTokens** compara dos [*tokens*](/windows/desktop/SecGloss/a-gly) de acceso y determina si son equivalentes con respecto a una llamada a la [**función AccessCheck.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FirstTokenHandle* \[ En\]
</dt> <dd>

Identificador del primer token de acceso que se comparará. El token debe estar abierto para el **acceso a TOKEN \_ QUERY.**

</dd> <dt>

*SecondTokenHandle* \[ En\]
</dt> <dd>

Identificador del segundo token de acceso que se comparará. El token debe estar abierto para el **acceso a TOKEN \_ QUERY.**

</dd> <dt>

*Igual a* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un valor que indica si los tokens representados por los parámetros *FirstTokenHandle* y *SecondTokenHandle* son equivalentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve STATUS \_ SUCCESS.

Si se produce un error en la función, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

Dos tokens de control de acceso se consideran equivalentes si se cumplen todas las condiciones siguientes:

-   Todos [*los identificadores*](/windows/desktop/SecGloss/s-gly) de seguridad (SID) presentes en cualquiera de los tokens también están presentes en el otro token.
-   Ninguno de los tokens o ambos están restringidos.
-   Si ambos tokens están restringidos, todos los SID restringidos en un token también se restringen en el otro token.
-   Todos los privilegios presentes en cualquiera de los tokens también están presentes en el otro token.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ntseapi.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

