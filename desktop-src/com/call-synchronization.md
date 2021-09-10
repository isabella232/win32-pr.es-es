---
title: Sincronización de llamadas
description: Sincronización de llamadas
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369448"
---
# <a name="call-synchronization"></a>Sincronización de llamadas

Las aplicaciones COM deben ser capaces de tratar correctamente la entrada del usuario al procesar una o varias llamadas desde COM o el sistema operativo. COM proporciona sincronización de llamadas solo para los departamentos de un solo subproceso. Los departamentos multiproceso (que contienen subprocesos de subproceso libre) no reciben llamadas al realizar llamadas (en el mismo subproceso). Los departamentos multiproceso no pueden realizar llamadas sincronizadas de entrada. Las llamadas asincrónicas se convierten en llamadas sincrónicas en los departamentos multiproceso. No se llama al filtro de mensajes para ningún subproceso de un apartamento multiproceso. Para obtener más información sobre los problemas de subprocesos, vea [Procesos, subprocesos y departamentos](processes--threads--and-apartments.md).

Las llamadas COM entre procesos se divide en tres categorías, como se muestra a continuación:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Llamadas sincrónicas*
</dt> <dd>

La mayor parte de la comunicación que tiene lugar dentro de COM es sincrónica. Al realizar llamadas sincrónicas, el autor de la llamada espera la respuesta antes de continuar y puede recibir mensajes entrantes mientras espera. COM entra en un bucle modal para esperar la respuesta, recibiendo y distribuyendo otros mensajes de forma controlada.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notificaciones asincrónicas*
</dt> <dd>

Al enviar notificaciones asincrónicas, el autor de la llamada no espera la respuesta. COM usa [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) o eventos de alto nivel para enviar notificaciones asincrónicas, en función de la plataforma. COM define cinco métodos asincrónicos [**de IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Mientras COM procesa una llamada asincrónica, no se pueden realizar llamadas sincrónicas. Por ejemplo, la implementación de [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) de una aplicación contenedora no puede contener una llamada a [**IPersistStorage::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Estas llamadas son las únicas llamadas asincrónicas admitidas por COM. No hay ninguna manera de crear una interfaz personalizada que sea asincrónica en este momento.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Llamadas sincronizadas con entrada*
</dt> <dd>

Al realizar llamadas sincronizadas con entrada, el objeto al que se llama debe completar la llamada antes de producir el control. Esto ayuda a garantizar que la administración del foco funciona correctamente y que los datos especificados por el usuario se procesan correctamente. Com realiza estas llamadas a través de la [**función SendMessage,**](/windows/win32/api/winuser/nf-winuser-sendmessage) sin entrar en un bucle modal. Al procesar una llamada sincronizada de entrada, el objeto al que se llama no debe llamar a ninguna función o método (incluidos los métodos sincrónicos) que puedan producir control. Los métodos siguientes se sincronizan con la entrada

-   [**IOleWindow::GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject::OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject::OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject::ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame::SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame::SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Para minimizar los problemas que pueden surgir del procesamiento asincrónico de mensajes, la mayoría de las llamadas al método COM son sincrónicas. Con la comunicación sincrónica, no es necesario que el código especial envíe y controle los mensajes entrantes. Cuando una aplicación realiza una llamada de método sincrónico, COM entra en un bucle de espera modal que controla las respuestas necesarias y envía los mensajes entrantes a las aplicaciones capaces de procesarlos.

COM administra las llamadas a métodos mediante la asignación de un identificador denominado identificador *de subproceso lógico*. Se asigna uno nuevo cuando un usuario selecciona un comando de menú o cuando la aplicación inicia una nueva operación COM. A las llamadas posteriores relacionadas con la llamada COM inicial se les asigna el mismo identificador de subproceso lógico que la llamada inicial.

 

 