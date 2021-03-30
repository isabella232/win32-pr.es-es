---
description: La función GetFrameCaptureHandle devuelve un identificador a la captura basada en un fotograma determinado.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Función GetFrameCaptureHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907671"
---
# <a name="getframecapturehandle-function"></a>GetFrameCaptureHandle función)

La función **GetFrameCaptureHandle** devuelve un identificador a la captura basada en un fotograma determinado.

## <a name="syntax"></a>Sintaxis


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador de un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador de la captura.

Si la función no se realiza correctamente, el valor devuelto es 0.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameCaptureHandle** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




