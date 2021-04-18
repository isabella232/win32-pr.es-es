---
description: Si un evento está disponible, el método NextEvent del objeto SWbemEventSource recupera el evento de una consulta de evento.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Método SWbemEventSource. NextEvent (Wbemdisp. h)
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
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707267"
---
# <a name="swbemeventsourcenextevent-method"></a>SWbemEventSource. NextEvent, método

Si un evento está disponible, el método **NextEvent** del objeto [**SWbemEventSource**](swbemeventsource.md) recupera el evento de una consulta de evento.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iTimeoutMs* \[ en, opcional\]
</dt> <dd>

Número de milisegundos que la llamada espera un evento antes de devolver un error de tiempo de espera. El valor predeterminado de este parámetro es **wbemTimeoutInfinite** (-1), que dirige la llamada para esperar indefinidamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método **NextEvent** se ejecuta correctamente, devuelve un objeto [**SWbemObject**](swbemobject.md) que contiene el evento solicitado. Si se agota el tiempo de espera de la llamada, el objeto devuelto es **null** y se produce un error.

## <a name="error-codes"></a>Códigos de error

Una vez finalizado el método **NextEvent** , el objeto **Err** puede contener el código de error de la lista siguiente.

<dl> <dt>

**wbemErrTimedOut** -0x80043001
</dt> <dd>

El evento solicitado no llegó en la cantidad de tiempo especificada en *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | \_ISWBEMEVENTSOURCE IID<br/>                                                       |



 

 




