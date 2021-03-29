---
description: La función GetCaptureTimeStamp devuelve la fecha y la hora en que la captura comenzó a grabar fotogramas.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Función GetCaptureTimeStamp (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540211"
---
# <a name="getcapturetimestamp-function"></a>GetCaptureTimeStamp función)

La función **GetCaptureTimeStamp** devuelve la fecha y la hora en que la captura comenzó a grabar fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ de\]
</dt> <dd>

Identificador de la captura. Para obtener información acerca de cómo obtener el identificador de captura, vea la sección Comentarios de este tema **GetCaptureTimeStamp** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a una estructura [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

La función **GetCaptureTimeStamp** devuelve la hora en que el proveedor de paquetes de red (NPP) comienza a recopilar datos, no cuando el experto carga la captura para su análisis.

No sobrescriba los datos en la estructura **SYSTEMTIME** . Los datos forman parte de la captura. Al intentar modificar los datos, se produce una infracción de acceso.

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureTimeStamp** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

