---
title: Compartimientos
description: Compartimientos
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Services Framework (TSF), compartimientos
- TSF (marco de trabajo de servicios de texto), compartimientos
- servicios de texto, compartimientos
- Aplicaciones habilitadas para TSF, compartimientos
- compartimientos
- Text Services Framework (TSF), tipos de compartimientos
- TSF (marco de trabajo de servicios de texto), tipos de compartimiento
- servicios de texto, tipos de compartimientos
- Aplicaciones habilitadas para TSF, tipos de compartimientos
- tipos de compartimientos
- Marco de trabajo de servicios de texto (TSF), notificaciones de cambios de compartimiento
- TSF (marco de trabajo de servicios de texto), notificaciones de cambios de compartimiento
- servicios de texto, notificaciones de cambios de compartimiento
- Aplicaciones habilitadas para TSF, notificaciones de cambios de compartimiento
- notificaciones de cambio de compartimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268530"
---
# <a name="compartments"></a>Compartimientos

## <a name="compartment-types"></a>Tipos de compartimientos

Hay varios tipos diferentes de compartimientos. Hay un compartimiento global, y cada administrador de subprocesos, administrador de documentos y contexto puede contener un compartimiento.

El compartimiento global permite a los clientes compartir datos entre procesos. Para obtener el administrador de compartimiento global, llame a [**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

El administrador de subprocesos contiene un administrador de compartimientos que contiene compartimientos por subproceso. Esto permite compartir los datos dentro de un subproceso. Para obtener un administrador de compartimientos del administrador de subprocesos, llame a **ITfThreadMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.

Cada administrador de documentos creado también contiene un administrador de compartimientos. Esto permite que los datos se compartan en un administrador de documentos específico. Para obtener el administrador de compartimientos del administrador de documentos, llame a **ITfDocumentMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.

Cada contexto creado también contiene un administrador de compartimientos. Esto permite que los datos se compartan en un contexto específico. Para obtener un administrador de compartimiento de contexto, llame a **ITfContext:: QueryInterface** con IID \_ ITfCompartmentMgr.

## <a name="creating-and-deleting-a-compartment"></a>Crear y eliminar un compartimiento

Se crea un compartimiento la primera vez que se llama a [**ITfCompartmentMgr:: GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) con el GUID del compartimiento. El cliente de instalación debe establecer el valor inicial del compartimiento mediante [**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Hasta que se establece un valor, el valor del compartimiento está vacío. Por esta razón, no hay ninguna manera de comprobar que el compartimiento existía antes de que se llamara a **GetCompartment** . Para evitar esta situación, el cliente de instalación debe establecer el valor en algún valor inicial para que otros clientes puedan determinar si el compartimiento ya existe.

El método [**ITfCompartmentMgr:: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) se usa para quitar un compartimiento. Las referencias existentes al compartimiento se marcan como no válidas.

## <a name="obtaining-compartments"></a>Obtener compartimientos

Mediante la interfaz [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , un cliente puede enumerar los compartimientos llamando a [**ITfCompartmentMgr:: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Este método proporciona un objeto **IEnumGUID** que contiene los GUID de todos los compartimientos instalados.

Con el GUID de compartimiento, se usa **ITfCompartmentMgr:: GetCompartment** para obtener un compartimiento específico. Este método proporciona al llamador un objeto [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) que puede obtener y establecer los datos del compartimiento.

## <a name="receiving-compartment-change-notifications"></a>Recepción de notificaciones de cambio de compartimiento

Cuando el valor de un compartimiento cambia, el administrador de TSF notifica a todos los receptores de notificaciones instalados que el compartimiento ha cambiado. Para instalar un receptor de notificaciones de cambio de compartimiento, cree un objeto que implemente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink). Después, llame a **ITfCompartment:: QueryInterface** con IID \_ ITfSource en el objeto de compartimiento que se va a supervisar para obtener una interfaz [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) . Ahora, llame a [**ITfSource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfCompartmentEventSink y el puntero al objeto **ITfCompartmentEventSink** . Cuando cambia el valor del compartimiento, se llama a [**ITfCompartmentEventSink:: onchange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) del receptor de notificaciones con el GUID del compartimiento. El receptor de notificaciones puede llamar a [**ITfCompartment:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) para obtener el nuevo valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**TfClientId**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink:: onchange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




