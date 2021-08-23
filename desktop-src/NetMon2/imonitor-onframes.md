---
description: El monitor debe implementar el método OnFrames. MCSVC llama a este método cuando el búfer de captura está lleno o ha transcurrido el tiempo de actualización.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: Método IMonitor::OnFrames (Netmon.h)
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
ms.openlocfilehash: a4138c35384753c8df79728a61decf78bf302d0dc9c0a71ca9f787d76a70a620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779175"
---
# <a name="imonitoronframes-method"></a>IMonitor::OnFrames (método)

El monitor debe implementar el método **OnFrames.** MCSVC llama a este método cuando el búfer de captura está lleno o ha transcurrido el tiempo de actualización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Evento* \[ En\]
</dt> <dd>

[UPDATE \_ Estructura EVENT](update-event.md) que contiene la información de marco utilizada para actualizar eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S \_ OK (que es el mismo que NOERROR). MCSVC devuelve el valor devuelto al NPP para su procesamiento.

Si el método no se realiza correctamente, el valor devuelto es un código de error. MCSVC devuelve el valor devuelto al NPP para su procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




