---
title: Compartimientos
description: Compartimientos
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Services Framework (TSF), compartimientos
- TSF (Text Services Framework), compartimientos
- servicios de texto, compartimientos
- Aplicaciones habilitadas para TSF, compartimientos
- Compartimientos
- Text Services Framework (TSF), tipos de compartimiento
- TSF (Text Services Framework), tipos de compartimiento
- servicios de texto, tipos de compartimiento
- Aplicaciones habilitadas para TSF, tipos de compartimiento
- tipos de compartimiento
- Text Services Framework (TSF), notificaciones de cambio de compartimiento
- TSF (Text Services Framework), notificaciones de cambio de compartimiento
- servicios de texto, notificaciones de cambio de compartimiento
- Aplicaciones habilitadas para TSF, notificaciones de cambio de compartimiento
- notificaciones de cambio de compartimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243705"
---
# <a name="compartments"></a>Compartimientos

## <a name="compartment-types"></a>Tipos de compartimiento

Hay varios tipos diferentes de compartimientos. Hay un compartimiento global y cada administrador de subprocesos, administrador de documentos y contexto puede contener un compartimiento.

El compartimiento global permite a los clientes compartir datos entre procesos. Para obtener el administrador global de compartimientos, llame [**a ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

El administrador de subprocesos contiene un administrador de compartimientos que contiene compartimientos por subproceso. Esto permite que los datos se compartan dentro de un subproceso. Para obtener un administrador de compartimientos del administrador de subprocesos, llame a **ITfThreadMgr::QueryInterface** con \_ IID ITfCompartmentMgr.

Cada administrador de documentos creado también contiene un administrador de compartimientos. Esto permite compartir datos dentro de un administrador de documentos específico. Para obtener el administrador de compartimientos del administrador de documentos, llame a **ITfDocumentMgr::QueryInterface** con \_ IID ITfCompartmentMgr.

Cada contexto creado también contiene un administrador de compartimientos. Esto permite compartir datos dentro de un contexto específico. Para obtener un administrador de compartimientos de contexto, llame **a ITfContext::QueryInterface** con \_ IID ITfCompartmentMgr.

## <a name="creating-and-deleting-a-compartment"></a>Creación y eliminación de un compartimiento

Se crea un compartimiento la primera vez que se llama a [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) con el GUID del compartimiento. El cliente de instalación debe establecer el valor inicial del compartimiento mediante [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Hasta que se establece un valor, el valor del compartimiento está vacío. Por este problema, no hay ninguna manera de comprobar que el compartimiento existía antes de llamar a **GetCompartment.** Para evitar esta situación, el cliente de instalación debe establecer el valor en algún valor inicial para que otros clientes puedan determinar si el compartimiento ya existe.

El [**método ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) se usa para quitar un compartimiento. Las referencias existentes al compartimiento se marcan como no válidas.

## <a name="obtaining-compartments"></a>Obtención de compartimientos

Mediante la [**interfaz ITfCompartmentMgr,**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) un cliente puede enumerar los compartimientos llamando a [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Este método proporciona un **objeto IEnumGUID** que contiene los GUID de todos los compartimientos instalados.

Con el GUID del compartimiento, **se usa ITfCompartmentMgr::GetCompartment** para obtener un compartimiento específico. Este método proporciona al autor de la llamada [**un objeto ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) que puede obtener y establecer los datos del compartimiento.

## <a name="receiving-compartment-change-notifications"></a>Recepción de notificaciones de cambio de compartimiento

Cuando cambia el valor de un compartimiento, el administrador de TSF notifica a los receptores de aviso instalados que el compartimiento ha cambiado. Para instalar un receptor de aviso de cambio de compartimiento, cree un objeto que implemente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink). A continuación, llame a **ITfCompartment::QueryInterface** con IID ITfSource en el objeto de compartimiento que se va a supervisar para obtener \_ una interfaz [**ITfSource.**](/windows/desktop/api/Msctf/nn-msctf-itfsource) Ahora llame [**a ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID ITfCompartmentEventSink y el puntero al \_ objeto **ITfCompartmentEventSink.** Cuando cambia el valor del compartimiento, se llama al [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) del receptor de aviso con el GUID del compartimiento. El receptor de notificaciones puede [**llamar a ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) para obtener el nuevo valor.

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

[**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




