---
UID: ''
title: Función CaptureStackBackTrace
description: Captura un seguimiento de la pila de nuevo recorrindo la pila.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279509"
---
# <a name="capturestackbacktrace-function"></a>Función CaptureStackBackTrace

## <a name="description"></a>Description

Captura un seguimiento de la pila de nuevo recorrindo la pila y registrando la información de cada fotograma.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Parámetros

### <a name="framestoskip-in"></a>FramesToSkip [in]

Número de fotogramas que se omitirán desde el inicio del seguimiento posterior.

### <a name="framestocapture-in"></a>FramesToCapture [in]

Número de fotogramas que se capturarán.
Puede capturar hasta fotogramas **MAXUSHORT.**

**Windows Server 2003 y Windows XP:**  La suma de los *parámetros FramesToSkip* y *FramesToCapture* debe ser inferior a 63.

### <a name="backtrace-out"></a>BackTrace [out]

Matriz de punteros capturada del seguimiento de pila actual.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, optional]

Valor que se puede usar para organizar las tablas hash.
Si este parámetro es **NULL,** no se calcula ningún valor hash.

Este valor se calcula en función de los valores de los punteros devueltos en la matriz BackTrace.
Dos seguimientos de pila idénticos generarán valores hash idénticos.

## <a name="returns"></a>Devoluciones

Número de fotogramas capturados.

## <a name="remarks"></a>Comentarios

La **función CaptureStackBackTrace** se define como la función **RtlCaptureStackBackTrace** (la definición se incluye en el SDK de Windows a partir de Windows Vista).
Para obtener más información, consulta WinBase.h y WinNT.h.

## <a name="see-also"></a>Consulte también
