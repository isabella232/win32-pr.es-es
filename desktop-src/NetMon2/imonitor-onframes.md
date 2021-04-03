---
description: El monitor debe implementar el método biframes. MCSVC llama a este método cuando el búfer de captura está lleno o se ha superado el tiempo de actualización.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'IMonitor:: biframes (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809464"
---
# <a name="imonitoronframes-method"></a>IMonitor:: alframes (método)

El monitor debe implementar el método **Biframes** . MCSVC llama a este método cuando el búfer de captura está lleno o se ha superado el tiempo de actualización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Evento* \[ de de\]
</dt> <dd>

[Actualización \_ de ](update-event.md) Estructura de eventos que contiene la información del marco utilizada para actualizar los eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError). El MCSVC devuelve el valor devuelto a NPP para su procesamiento.

Si el método no se realiza correctamente, el valor devuelto es un código de error. El MCSVC devuelve el valor devuelto a NPP para su procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




