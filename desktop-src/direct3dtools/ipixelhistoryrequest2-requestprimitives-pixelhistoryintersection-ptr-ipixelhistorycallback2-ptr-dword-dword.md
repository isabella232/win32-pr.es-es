---
description: Solicita una lista de primitivas de una intersección determinada. Para obtener más información, vea la función miembro RequestIntersections.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2:: RequestPrimitives (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714703"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2:: RequestPrimitives (método)

Solicita una lista de primitivas de una intersección determinada. Para obtener más información, vea la función miembro RequestIntersections.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*intersección*   
Dirección de la intersección especificada.

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

 

 
