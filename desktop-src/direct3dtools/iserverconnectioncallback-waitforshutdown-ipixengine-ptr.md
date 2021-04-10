---
description: Esperar el cierre del motor especificado (llamada de bloqueo).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IServerConnectionCallback:: WaitForShutdown (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152614"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>IServerConnectionCallback:: WaitForShutdown (método)

Esperar el cierre del motor especificado (llamada de bloqueo).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a>Parámetros

*pEngine*   
Motor que se va a cerrar.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IServerConnectionCallback**](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
