---
description: Devolución de llamada que notifica al host qué fases de canalización no pueden devolver datos de malla para el evento especificado en la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback::MeshDataNotAvailableCallback (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c95f661c5a18f2573fe477f3aa1ef4d0035ee1e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622141"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback (método)

Devolución de llamada que notifica al host qué fases de canalización no pueden devolver datos de malla para el evento especificado en la solicitud asociada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a>Parámetros

*numberStages*   
Número de errores de fase devueltos.

*errores \_ count0*   
Errores de la fase de canalización.

*Ancho*   
Ancho de la cadena de intercambio con la llamada a draw. Esto se usa al solicitar imágenes de vista previa de canalización.

*Altura*   
Alto de la cadena de intercambio con la llamada a draw. Esto se usa al solicitar imágenes de vista previa de canalización.

*Eid*   
Evento representado en los resultados.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
