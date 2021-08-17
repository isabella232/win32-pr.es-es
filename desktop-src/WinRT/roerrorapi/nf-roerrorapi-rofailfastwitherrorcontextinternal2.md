---
title: Función RoFailFastWithErrorContextInternal2
description: Genera una excepción no continuable en el proceso actual y también permite incluir contextos de error adicionales que el sistema operativo aún no ha capturado.
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
ms.openlocfilehash: a2e8e2e357b7c4768596ca36cb48cdf1bb2cfdbd839ecc6949a607975d6000c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560631"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>Función RoFailFastWithErrorContextInternal2

Genera una excepción no continuable en el proceso actual y también permite incluir contextos de error adicionales que el sistema operativo (SO) aún no ha capturado.

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

HRESULT **asociado** al error actual. La excepción se produce para cualquier valor *de hrError.*

`cStowedExceptions`

Tipo: **[ULONG](../../winprog/windows-data-types.md)**

Número de elementos de la *matriz aStowedExceptionPointers.*

`aStowedExceptionPointers`

Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Matriz de punteros a [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) estructuras. Cada estructura contiene información que describe una excepción stowed. A continuación, la información de estas estructuras se envía a Informe de errores de Windows (WER) junto con la información de excepción stowed capturada por la plataforma.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.

## <a name="remarks"></a>Comentarios

**RoFailFastWithErrorContextInternal2** no está asociado a una biblioteca de importación ni a un archivo de encabezado. Puede llamarla primero mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (para cargar ) y, a continuación, llamando a la función GetProcAddress para recuperar la dirección `ComBase.dll` de **RoFailFastWithErrorContextInternal2**. [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Para obtener más información, [vea Función RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | N/D |
| **Library** | N/D |
| **Dll** | ComBase.dll |

## <a name="see-also"></a>Consulte también

* [Función RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)