---
description: El mensaje TAPI LINE CALLINFO se envía cuando ha cambiado la información de llamada \_ sobre la llamada especificada. La aplicación puede invocar lineGetCallInfo para determinar la información de llamada actual.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: LINE_CALLINFO mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250215"
---
# <a name="line_callinfo-message"></a>Mensaje \_ LINE CALLINFO

El mensaje TAPI **LINE \_ CALLINFO** se envía cuando ha cambiado la información de llamada sobre la llamada especificada. La aplicación puede invocar [**lineGetCallInfo para**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) determinar la información de llamada actual.


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

Elemento de información de llamada que ha cambiado. Puede ser una o varias de las [**constantes LINECALLINFOSTATE \_**](linecallinfostate--constants.md).

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

Se envía un mensaje **LINE \_ CALLINFO** con una indicación *NumOwnersIncr*, *NumOwnersDecr* o *NumMonitorsChanged* a las aplicaciones que ya tienen un identificador para la llamada. Esto puede ser el resultado de que otra aplicación cambie la propiedad o la supervisión a una llamada con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown,**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) [**lineSetCallPrivilege,**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)y [**lineGetConfRelatedCalls.**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)

Estos **mensajes LINE \_ CALLINFO** no se envían cuando se proporciona una notificación de una nueva llamada en un mensaje LINE CALLSTATE, porque la información de llamada ya refleja el número correcto de propietarios y monitores en el momento en que se envían los mensajes LINE [**\_ CALLSTATE.**](line-callstate.md) \_ **LÍNEA \_ Los mensajes CALLINFO** también se suprimen en el caso en que TAPI ofrece una llamada a los monitores a través del mecanismo LINECALLSTATE \_ UNKNOWN.

> [!Note]  
> La aplicación que provoca un cambio en el número de propietarios o monitores (por ejemplo, mediante la invocación de [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) o [**lineSetCallPrivilege)**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)no recibe por sí misma un mensaje que indica que el cambio se ha realizado.

 

No se envía ningún mensaje **LINE \_ CALLINFO** para una llamada después de que la llamada haya entrado en el *estado de* inactividad. En concreto, los cambios en el número de propietarios y monitores no se notifican cuando las aplicaciones desasignan sus identificadores para la llamada inactiva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 




