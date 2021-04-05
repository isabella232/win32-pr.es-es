---
title: Sincronización de llamadas
description: Sincronización de llamadas
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078435"
---
# <a name="call-synchronization"></a>Sincronización de llamadas

Las aplicaciones COM deben ser capaces de tratar correctamente con los datos proporcionados por el usuario al procesar una o más llamadas de COM o del sistema operativo. COM permite la sincronización de llamadas para apartamentos de un solo subproceso. Los apartamentos multiproceso (que contienen subprocesos de subprocesos libres) no reciben llamadas mientras realizan llamadas (en el mismo subproceso). Los apartamentos multiproceso no pueden realizar llamadas sincronizadas de entrada. Las llamadas asincrónicas se convierten en llamadas sincrónicas en apartamentos multiproceso. No se llama al filtro de mensajes para ningún subproceso de un apartamento multiproceso. Para obtener más información sobre los problemas de subprocesos, consulte [procesos, subprocesos y apartamentos](processes--threads--and-apartments.md).

Las llamadas COM entre procesos se dividen en tres categorías, como se indica a continuación:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Llamadas sincrónicas*
</dt> <dd>

La mayor parte de la comunicación que tiene lugar en COM es sincrónica. Al realizar llamadas sincrónicas, el autor de la llamada espera la respuesta antes de continuar y puede recibir los mensajes entrantes mientras se espera. COM escribe un bucle modal para esperar la respuesta, recibir y enviar otros mensajes de una manera controlada.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notificaciones asincrónicas*
</dt> <dd>

Cuando se envían notificaciones asincrónicas, el autor de la llamada no espera la respuesta. COM usa eventos [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) o de alto nivel para enviar notificaciones asincrónicas, dependiendo de la plataforma. COM define cinco métodos asincrónicos de [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Mientras COM está procesando una llamada asincrónica, no se pueden realizar llamadas sincrónicas. Por ejemplo, la implementación de [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) de una aplicación contenedora no puede contener una llamada a [**IPersistStorage:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Estas llamadas son las únicas llamadas asincrónicas admitidas por COM. En este momento no hay ninguna manera de crear una interfaz personalizada que sea asincrónica.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Llamadas de entrada sincronizadas*
</dt> <dd>

Al realizar llamadas sincronizadas de entrada, el objeto al que se llama debe completar la llamada antes de producir el control. Esto ayuda a garantizar que la administración del enfoque funciona correctamente y que los datos escritos por el usuario se procesan de forma adecuada. COM realiza estas llamadas a través de la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) , sin entrar en un bucle modal. Al procesar una llamada sincronizada de entrada, el objeto llamado no debe llamar a ninguna función o método (incluidos los métodos sincrónicos) que puedan producir el control. Los métodos siguientes son entradas sincronizadas

-   [**IOleWindow::GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject:: OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject:: OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject:: ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame:: SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame:: SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Para minimizar los problemas que pueden surgir en el procesamiento de mensajes asincrónicos, la mayoría de las llamadas a métodos COM son sincrónicas. Con la comunicación sincrónica, no es necesario que el código especial envíe y controle los mensajes entrantes. Cuando una aplicación realiza una llamada sincrónica al método, COM entra en un bucle de espera modal que controla las respuestas necesarias y envía los mensajes entrantes a las aplicaciones capaces de procesarlos.

COM administra las llamadas a métodos mediante la asignación de un identificador denominado *identificador de subproceso lógico*. Cuando un usuario selecciona un comando de menú o cuando la aplicación inicia una nueva operación COM, se asigna uno nuevo. A las llamadas subsiguientes relacionadas con la llamada a COM inicial se les asigna el mismo identificador de subproceso lógico que la llamada inicial.

 

 