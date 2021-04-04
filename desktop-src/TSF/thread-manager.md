---
title: Administrador de subprocesos
description: El administrador de subprocesos es el componente base del administrador de TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Marco de trabajo de servicios de texto (TSF), administrador de subprocesos
- TSF (marco de trabajo de servicios de texto), administrador de subprocesos
- servicios de texto, administrador de subprocesos
- Aplicaciones habilitadas para TSF, administrador de subprocesos
- Administrador de subprocesos
- Administrador de TSF
- notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077999"
---
# <a name="thread-manager"></a>Administrador de subprocesos

El administrador de subprocesos es el componente base del administrador de TSF. El administrador de subprocesos realiza tareas comunes relacionadas con aplicaciones y servicios de texto (clientes). Estas tareas incluyen, entre otras, la activación y desactivación de los servicios de texto TSF, la creación de administradores de documentos y el mantenimiento de la relación adecuada entre documentos y el foco de entrada. El administrador de subprocesos se define mediante la interfaz [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .

La mayoría de las interfaces y los objetos proporcionados por el administrador de TSF se pueden obtener utilizando los métodos proporcionados por la interfaz del administrador de subprocesos.

## <a name="applications"></a>APLICACIONES

Una aplicación crea un objeto administrador de subprocesos llamando a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ TFThreadMgr.

## <a name="text-services"></a>Servicios de texto

Un servicio de texto obtiene un objeto de administrador de subprocesos en el método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servicio de texto.

## <a name="event-notifications"></a>Notificaciones de eventos

El administrador de subprocesos también proporciona la notificación de eventos a los clientes. En TSF, las notificaciones de eventos se proporcionan por medio de un receptor de eventos, que es un objeto COM. Para recibir notificaciones del administrador de subprocesos, un cliente implementa un objeto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e instala el receptor de eventos. El receptor de eventos se instala consultando el administrador de subprocesos para IID \_ ITfSource y llamando a [ITfSource:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfThreadMgrEventSink.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 