---
description: Compara dos tokens de acceso y determina si son equivalentes con respecto a una llamada a la función AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Función NtCompareTokens (Ntseapi. h)
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
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652563"
---
# <a name="ntcomparetokens-function"></a>NtCompareTokens función)

La función **NtCompareTokens** compara dos [*tokens de acceso*](/windows/desktop/SecGloss/a-gly) y determina si son equivalentes con respecto a una llamada a la función [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .

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

*FirstTokenHandle* \[ de\]
</dt> <dd>

Identificador del primer token de acceso que se va a comparar. El token debe estar abierto para el acceso a la **\_ consulta de tokens** .

</dd> <dt>

*SecondTokenHandle* \[ de\]
</dt> <dd>

Identificador del segundo token de acceso que se va a comparar. El token debe estar abierto para el acceso a la **\_ consulta de tokens** .

</dd> <dt>

*Igual* \[ a enuncia\]
</dt> <dd>

Un puntero a una variable que recibe un valor que indica si los tokens representados por los parámetros *FirstTokenHandle* y *SecondTokenHandle* son equivalentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve el estado \_ Success.

Si se produce un error en la función, devuelve un código de error **NTSTATUS** .

## <a name="remarks"></a>Observaciones

Dos tokens de control de acceso se consideran equivalentes si se cumplen todas las condiciones siguientes:

-   Cada [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que se encuentra en cualquiera de los tokens también está presente en el otro token.
-   Ninguno de los tokens o ambos están restringidos.
-   Si ambos tokens están restringidos, todos los SID que están restringidos en un token también están restringidos en el otro token.
-   Cada privilegio presente en cualquiera de los tokens también está presente en el otro token.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Ntseapi. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

