---
title: Método OnStatusChanged de IRemoteDesktopClientEvents (Locationapi.h)
description: Se llama cuando el control de cliente ha actualizado su estado.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Método OnStatusChanged Servicios de Escritorio remoto
- Método OnStatusChanged Servicios de Escritorio remoto , interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto método , OnStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073314"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>IRemoteDesktopClientEvents::OnStatusChanged (método)

Se llama cuando el control de cliente ha actualizado su estado.

## <a name="syntax"></a>Sintaxis


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*statusCode* 
</dt> <dd>

Nuevo código de estado.

</dd> <dt>

*statusMessage* 
</dt> <dd>

Texto del mensaje de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>Locationapi.h</dt> </dl>       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





