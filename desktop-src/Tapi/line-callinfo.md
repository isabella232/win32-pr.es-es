---
description: El mensaje de línea de \_ CALLINFO TAPI se envía cuando ha cambiado la información de llamada sobre la llamada especificada. La aplicación puede invocar lineGetCallInfo para determinar la información de la llamada actual.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Mensaje de LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690401"
---
# <a name="line_callinfo-message"></a>Mensaje de línea \_ CALLINFO

El mensaje de **línea de \_ CALLINFO** TAPI se envía cuando ha cambiado la información de llamada sobre la llamada especificada. La aplicación puede invocar [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar la información de la llamada actual.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la llamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Elemento de información de llamada que ha cambiado. Puede ser una o varias de las [**\_ constantes LINECALLINFOSTATE**](linecallinfostate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se envía un mensaje **line \_ CALLINFO** con una indicación *NumOwnersIncr*, *NumOwnersDecr* y/o *NumMonitorsChanged* a las aplicaciones que ya tienen un identificador para la llamada. Esto puede ser el resultado de que otra aplicación cambie la propiedad o supervise una llamada con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)y [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).

Estos mensajes de **línea \_ CALLINFO** no se envían cuando se proporciona una notificación de una nueva llamada en un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) , ya que la información de la llamada ya refleja el número correcto de propietarios y monitores en el momento en que \_ se envían los mensajes de CALLSTATE de línea. **Línea \_ de** Los mensajes CALLINFO también se suprimen en el caso de que TAPI ofrezca una llamada para que supervise a través del \_ mecanismo desconocido de LINECALLSTATE.

> [!Note]  
> La aplicación que provoca un cambio en el número de propietarios o monitores (por ejemplo, mediante la invocación de [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) o [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) no recibe un mensaje que indica que se ha realizado el cambio.

 

No se envía ningún mensaje de **línea \_ CALLINFO** para una llamada después de que la llamada haya entrado en el estado de *inactividad* . En concreto, los cambios en el número de propietarios y monitores no se informan como aplicaciones que desasignan sus identificadores para la llamada inactiva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




