---
description: Función de devolución de llamada que se usa para notificar el progreso del host de los motores. Esto también sirve como una manera para que el host determine que el motor todavía se está ejecutando.
title: 'IStatusCallback:: status (método)'
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
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714747"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback:: status (método)

Función de devolución de llamada que se usa para notificar al host el progreso del motor. Esto también sirve como una manera para que el host determine que el motor todavía se está ejecutando.

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
Tiempo transcurrido desde la última llamada al estado, en milisegundos.

*dwFramesCaptured*   
Número de fotogramas que se han capturado desde la última llamada al estado.

*dwFramesElapsed*   
Número de fotogramas transcurridos desde la última llamada al estado.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
