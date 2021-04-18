---
description: Inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interfaz IWbemEventSink (Wbemprov. h)
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
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706843"
---
# <a name="iwbemeventsink-interface"></a>Interfaz IWbemEventSink

La interfaz **IWbemEventSink** inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas. Esta interfaz extiende [**IWbemObjectSink**](iwbemobjectsink.md), lo que proporciona nuevos métodos que se ocupan de la seguridad y el rendimiento. Para obtener más información sobre el uso de esta interfaz, vea [escribir un proveedor de eventos](writing-an-event-provider.md) y [proteger eventos de WMI](securing-wmi-events.md).

## <a name="members"></a>Miembros

La interfaz **IWbemEventSink** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWbemEventSink** tiene estos métodos.



| Método                                                                | Descripción                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Lo llama el consumidor para configurar consultas de eventos restringidos.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Comprueba el estado del receptor de eventos.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Lo llama el consumidor para establecer los parámetros de procesamiento por lotes.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Se utiliza para actualizar el descriptor de seguridad de un receptor de eventos.<br/>   |



 

## <a name="remarks"></a>Observaciones

Al implementar un receptor de suscripciones de eventos ([**IWbemObjectSink**](iwbemobjectsink.md) o **IWbemEventSink**), no llame a WMI desde los métodos del objeto receptor. Por ejemplo, la llamada a [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar el receptor desde una implementación de [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) puede interferir con el estado de WMI. Para cancelar una suscripción de eventos, establezca una marca y llame a **IWbemServices:: CancelAsyncCall** desde otro subproceso u objeto. En el caso de las implementaciones que no están relacionadas con un receptor de eventos, como las recuperaciones de objetos, enumeraciones y consultas, puede volver a llamar a WMI.

Las implementaciones de receptores deben procesar la notificación de eventos en un plazo de 100 MS, ya que el subproceso de WMI que entrega la notificación de eventos no puede realizar otras tareas hasta que el objeto receptor haya completado el procesamiento. Si la notificación requiere una gran cantidad de procesamiento, el receptor puede utilizar una cola interna para que otro subproceso controle el procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                            |
| Encabezado<br/>                   | <dl> <dt>Wbemprov. h (incluye Wbemidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




