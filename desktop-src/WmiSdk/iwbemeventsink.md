---
description: Inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interfaz IWbemEventSink (Wbemprov.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 10c5fa56a96db3e46ce2c4c7941fd7a1d6fb27a1730dc3741890935782e4ace7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318101"
---
# <a name="iwbemeventsink-interface"></a>Interfaz IWbemEventSink

La **interfaz IWbemEventSink** inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas. Esta interfaz amplía [**IWbemObjectSink,**](iwbemobjectsink.md)proporcionando nuevos métodos que se ocupa de la seguridad y el rendimiento. Para obtener más información sobre el uso de esta interfaz, vea [Escribir un proveedor de eventos](writing-an-event-provider.md) y Proteger eventos [WMI](securing-wmi-events.md).

## <a name="members"></a>Miembros

La **interfaz IWbemEventSink** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWbemEventSink** tiene estos métodos.



| Método                                                                | Descripción                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Llamado por el consumidor para configurar consultas de eventos restringidos.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Comprueba el estado del receptor de eventos.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Llamado por el consumidor para establecer parámetros de procesamiento por lotes.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Se usa para actualizar el descriptor de seguridad en un receptor de eventos.<br/>   |



 

## <a name="remarks"></a>Comentarios

Al implementar un receptor de suscripción de eventos ([**IWbemObjectSink**](iwbemobjectsink.md) **o IWbemEventSink**), no llame a WMI desde dentro de los métodos del objeto receptor. Por ejemplo, llamar a [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar el receptor desde una implementación de [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) puede interferir con el estado wmi. Para cancelar una suscripción de eventos, establezca una marca y llame a **IWbemServices::CancelAsyncCall** desde otro subproceso u objeto. Para las implementaciones que no están relacionadas con un receptor de eventos, como recuperaciones de objetos, enumeraciones y consultas, puede volver a llamar a WMI.

Las implementaciones de receptor deben procesar la notificación de eventos en un plazo de 100 MSEC porque el subproceso WMI que entrega la notificación de eventos no puede realizar otro trabajo hasta que el objeto receptor haya completado el procesamiento. Si la notificación requiere una gran cantidad de procesamiento, el receptor puede usar una cola interna para que otro subproceso controle el procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                            |
| Header<br/>                   | <dl> <dt>Wbemprov.h (incluir Wbemidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




