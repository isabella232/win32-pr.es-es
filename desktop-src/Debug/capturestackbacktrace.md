---
UID: ''
title: CaptureStackBackTrace función)
description: Captura un seguimiento de la pila de retroceso recorriendo la pila.
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
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "105656307"
---
# <a name="capturestackbacktrace-function"></a>CaptureStackBackTrace función)

## <a name="description"></a>Descripción

Captura un seguimiento de la pila de retroceso recorriendo la pila y grabando la información de cada fotograma.

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

Número de fotogramas que se van a omitir desde el inicio del seguimiento de la copia de seguridad.

### <a name="framestocapture-in"></a>FramesToCapture [in]

Número de fotogramas que se van a capturar.
Puede capturar hasta **MAXUSHORT** fotogramas.

**Windows Server 2003 y Windows XP:**  La suma de los parámetros *FramesToSkip* y *FramesToCapture* debe ser inferior a 63.

### <a name="backtrace-out"></a>Paseguir [out]

Matriz de punteros capturados del seguimiento de pila actual.

### <a name="backtracehash-out-optional"></a>BackTraceHash [out, opcional]

Valor que se puede utilizar para organizar las tablas hash.
Si este parámetro es **null**, no se calcula ningún valor hash.

Este valor se calcula en función de los valores de los punteros devueltos en la matriz de subseguimiento.
Dos seguimientos de pila idénticos generarán valores hash idénticos.

## <a name="returns"></a>Devoluciones

Número de fotogramas capturados.

## <a name="remarks"></a>Observaciones

La función **CaptureStackBackTrace** se define como la función **RtlCaptureStackBackTrace** (la definición se incluye en el Windows SDK a partir de Windows Vista).
Para obtener más información, vea WinBase. h y Winnt. h.

## <a name="see-also"></a>Vea también
