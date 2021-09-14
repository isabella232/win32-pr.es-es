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
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169338"
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

## <a name="remarks"></a>Observaciones

La **función GetCaptureTimeStamp** devuelve la hora a la que el proveedor de paquetes de red (NPP) comienza a recopilar datos, no cuando el experto carga la captura para su análisis.

No sobrescriba los datos de la **estructura SYSTEMTIME.** Los datos forman parte de la captura. Al intentar modificar los datos, se produce una infracción de acceso.

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetCaptureTimeStamp.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

