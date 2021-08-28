---
description: Solicitudes para obtener información sobre qué columnas (campos) admite este tipo de solicitud de tabla de objetos.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableRequest::RequestSupportedColumnsAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bfdf3b488296cf0092f59d4b944c39e00df45e31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629588"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync (método)

Solicitudes para obtener información sobre qué columnas (campos) admite este tipo de solicitud de tabla de objetos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*requestCallback*   
Dirección de devolución de llamada utilizada para notificar al host de resultados.

*progressIntervalMsecs*   
No se utiliza.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IObjectTableRequest**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
