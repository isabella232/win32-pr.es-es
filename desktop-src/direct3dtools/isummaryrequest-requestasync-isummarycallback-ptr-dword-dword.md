---
description: Una solicitud asincrónica para obtener información de resumen sobre un registro de gráficos.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISummaryRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714744"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest:: RequestAsync (método)

Una solicitud asincrónica para obtener información de resumen sobre un registro de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

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

[**ISummaryRequest**](/windows/desktop/direct3dtools/isummaryrequest)

 

 
