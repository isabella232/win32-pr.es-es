---
title: RoFailFastWithErrorContextInternal2 función)
description: Genera una excepción no continuada en el proceso actual y también permite incluir el contexto de error adicional aún no capturado por el sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105720182"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>RoFailFastWithErrorContextInternal2 función)

Genera una excepción no continuada en el proceso actual y también permite incluir el contexto de error adicional aún no capturado por el sistema operativo (SO).

## <a name="syntax"></a>Sintaxis

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>Parámetros

`hrError`

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

**HRESULT** asociado al error actual. La excepción se produce para cualquier valor de *hrError*.

`cStowedExceptions`

Tipo: **[ULong](../../winprog/windows-data-types.md)**

Número de elementos de la matriz *aStowedExceptionPointers* .

`aStowedExceptionPointers`

Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Matriz de punteros a estructuras de [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) . Cada estructura contiene información que describe una excepción estibada. La información de estas estructuras se envía a Informe de errores de Windows (WER) junto con la información de excepción estibada capturada por la plataforma.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.

## <a name="remarks"></a>Observaciones

**RoFailFastWithErrorContextInternal2** no está asociado a una biblioteca de importación ni a un archivo de encabezado. Puede llamarlo primero mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (para cargar `ComBase.dll` ) y, a continuación, llamando a la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar la dirección de **RoFailFastWithErrorContextInternal2**.

Para obtener más información, consulte [función RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | N/D |
| **Library** | N/D |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>Vea también

* [RoFailFastWithErrorContext función)](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)