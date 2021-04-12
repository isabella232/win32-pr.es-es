---
description: Conéctese a otra instancia de un motor remoto en el equipo local.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IServerConnectionCallback:: ConnectToEngine (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152615"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback:: ConnectToEngine (método)

Conéctese a otra instancia de un motor remoto en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a>Parámetros

*bLegacyConnection*   
True si el motor utiliza es heredado; de lo contrario, false.

*runAddress*   
Cadena COM que contiene el nombre del equipo local.

*ppEngineCreated*   
En la devolución, la dirección de la instancia del motor.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IServerConnectionCallback**](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
