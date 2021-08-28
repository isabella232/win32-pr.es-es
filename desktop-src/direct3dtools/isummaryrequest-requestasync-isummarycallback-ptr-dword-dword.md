---
description: Solicitud asincrónica para obtener información de resumen sobre un registro de gráficos.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISummaryRequest::RequestAsync (método)
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
ms.openlocfilehash: 0b754ced8a25464d57f2b7a3602e07a16b382a5c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624891"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync (método)

Solicitud asincrónica para obtener información de resumen sobre un registro de gráficos.

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
Dirección de devolución de llamada usada para notificar al host de resultados.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se utiliza.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**ISummaryRequest**](/windows/desktop/direct3dtools/isummaryrequest)

 

 
