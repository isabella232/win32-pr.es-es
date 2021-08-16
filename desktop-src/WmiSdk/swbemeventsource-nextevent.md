---
description: Si hay un evento disponible, el método NextEvent del objeto SWbemEventSource recupera el evento de una consulta de eventos.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Método SWbemEventSource.NextEvent (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6ce39d442b48f32c2aafcd6e24c1c214dce82a19435b6b36bce65d5426161859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050073"
---
# <a name="swbemeventsourcenextevent-method"></a>Método SWbemEventSource.NextEvent

Si hay un evento disponible, el **método NextEvent** del objeto [**SWbemEventSource**](swbemeventsource.md) recupera el evento de una consulta de eventos.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iTimeoutMs* \[ in, opcional\]
</dt> <dd>

Número de milisegundos que la llamada espera un evento antes de devolver un error de tiempo de espera. El valor predeterminado de este parámetro es **wbemTimeoutInfinite** (-1), que dirige la llamada a esperar indefinidamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el **método NextEvent** es correcto, devuelve un [**objeto SWbemObject**](swbemobject.md) que contiene el evento solicitado. Si se produce un tiempo de espera de la llamada, el objeto devuelto **es NULL** y se genera un error.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método NextEvent,** el **objeto Err** puede contener el código de error en la lista siguiente.

<dl> <dt>

**wbemErrTimedOut** : 0x80043001
</dt> <dd>

El evento solicitado no llegó en la cantidad de tiempo especificada en *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



 

 




