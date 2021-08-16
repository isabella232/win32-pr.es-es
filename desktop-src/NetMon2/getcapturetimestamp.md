---
description: La función GetCaptureTimeStamp devuelve la hora y la fecha en que la captura inició la grabación de fotogramas.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Función GetCaptureTimeStamp (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 93ae1c94a5e83d0029aba4403ad4ba23db0f4006bb5b9be68cc469939e63c734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366640"
---
# <a name="getcapturetimestamp-function"></a>Función GetCaptureTimeStamp

La **función GetCaptureTimeStamp** devuelve la hora y la fecha en que la captura inició la grabación de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ En\]
</dt> <dd>

Identificador de la captura. Para obtener información sobre cómo obtener el identificador de captura, vea la sección Comentarios de este **tema GetCaptureTimeStamp.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a una [estructura SYSTEMTIME.](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Comentarios

La **función GetCaptureTimeStamp** devuelve la hora en que el proveedor de paquetes de red (NPP) comienza a recopilar datos, no cuando el experto carga la captura para su análisis.

No sobrescriba los datos de la **estructura SYSTEMTIME.** Los datos forman parte de la captura. Al intentar modificar los datos, se produce una infracción de acceso.

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetCaptureTimeStamp.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

