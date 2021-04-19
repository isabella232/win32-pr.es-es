---
description: Solicita una lista de eventos que provocan un cambio en el píxel especificado, el destino de representación/UAV y el marco.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2:: RequestIntersections (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537318"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2:: RequestIntersections (método)

Solicita una lista de eventos que provocan un cambio en el píxel especificado, el destino de representación/UAV y el marco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*Númeromarco*   
Marco especificado.

*píxel*   
Píxel especificado.

*renderTargetPtr*   
Dirección del destino de representación especificado

*requestCallback*   
Dirección de devolución de llamada que se utiliza para notificar al host los resultados.

*requestCookie*   
Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.

*progressIntervalMsecs*   
No se utiliza.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixelHistoryRequest2**](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
