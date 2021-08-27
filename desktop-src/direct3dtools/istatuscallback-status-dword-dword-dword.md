---
description: Función de devolución de llamada que se usa para notificar al host del progreso de los motores. Esto también sirve como una manera de que el host determine que el motor todavía se está ejecutando.
title: IStatusCallback::Status (Método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: edf48e62389224a01af7e52aa7e87f3db63b3740
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622311"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status (Método)

Función de devolución de llamada que se usa para notificar al host el progreso del motor. Esto también sirve como una manera de que el host determine que el motor todavía se está ejecutando.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Parámetros

*dwMillisecondsElapsed*   
Tiempo transcurrido desde la última llamada a Estado, en milisegundos.

*dwFramesCaptured*   
Número de fotogramas que se han capturado desde la última llamada a Estado.

*dwFramesElapsed*   
Número de fotogramas transcurridos desde la última llamada a Estado.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
