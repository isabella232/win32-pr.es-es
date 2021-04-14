---
description: Un complemento de representador dinámico es un objeto que muestra los datos del lápiz de Tablet PC en tiempo real, tal como lo controla el objeto RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Complementos de Dynamic-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c3f1a33c3cd7faef2e899bcb198ea64aa5bd76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568920"
---
# <a name="dynamic-renderer-plug-ins"></a>Complementos de Dynamic-Renderer

Un complemento de representador dinámico es un objeto que muestra los datos del lápiz de Tablet PC en tiempo real, tal como lo controla el objeto [**RealTimeStylus**](realtimestylus-class.md) . Más adelante, para eventos como la actualización de un formulario, el complemento de representador dinámico o un complemento de recopilador de tintas puede volver a dibujar la tinta.

## <a name="the-dynamicrenderer-object"></a>El objeto DynamicRenderer

El objeto [**RealTimeStylus**](realtimestylus-class.md) implementa la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . El objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) representa la entrada de lápiz en tiempo real, a medida que se dibuja. Cuando se llama al método [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) mientras el objeto **DynamicRenderer** está habilitado, el objeto **DynamicRenderer** vuelve a dibujar el trazo que se está recopilando actualmente. La propiedad [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) del objeto **DynamicRenderer** está establecida inicialmente en **false**.

> [!Note]  
> Al llamar al método [**Refresh**](/previous-versions/ms826370(v=msdn.10)) del objeto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) desde un controlador de eventos [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) en código administrado, establezca la propiedad [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10)) del objeto **DynamicRenderer** en la propiedad [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) del objeto [PaintEventArgs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) .

 

El objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) puede almacenar temporalmente en memoria caché los datos de tinta. Para usar esta característica en código administrado, establezca la propiedad [EnableDataCache](/previous-versions/ms826349(v=msdn.10)) en **true**. Cuando el objeto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) recibe una llamada a su método [**IStylusSyncPlugin. StylusUp**](/previous-versions/ms826366(v=msdn.10)) , almacena en memoria caché los datos del trazo y agrega datos de lápiz personalizados a la cola de entrada en respuesta al objeto [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) del trazo. La propiedad [CustomDataId](/previous-versions/ms824749(v=msdn.10)) del objeto [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) se establece en el valor [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) y la propiedad data del objeto **CustomStylusData** contiene un objeto DynamicRendererCachedData. Llame al método [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) del objeto **DynamicRenderer** una vez que se haya recopilado el trazo y se pueda representar estáticamente. Cuando se llama al método [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) mientras el objeto **DynamicRenderer** está habilitado, el objeto **DynamicRenderer** vuelve a dibujar todos los trazos que están almacenados en caché. Cuando la propiedad [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) está establecida en **false**, los datos de trazo almacenados en caché se eliminan.

En el diagrama siguiente se ilustra cómo el objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) agrega datos a los datos del lápiz de Tablet PC cuando se establece la propiedad [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) del objeto **DynamicRenderer** .

![Ilustración que muestra el flujo de datos de DynamicRenderer](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

En este diagrama, el círculo con letra "SD" representa un objeto [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) y los círculos "P [**" representan objetos**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. El círculo "SU" representa un objeto [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónicos y, a continuación, se coloca en la cola de salida. La "recuperación ante desastres" de los círculos representa datos de lápiz personalizados que el complemento [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) agrega a la cola de entrada en respuesta a la notificación del lápiz hacia arriba asociada a "su". A continuación, la "recuperación ante desastres" de la carta del lápiz se pasa a los complementos sincrónicos y luego a la cola de salida antes de que se procesen los siguientes datos del lápiz de Tablet PC. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC. También se representa en el diagrama es el complemento del recopilador de tintas que llama al método [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) del objeto **DynamicRenderer** para liberar los datos del trazo almacenado en caché después de que el complemento de la colección de tintas haya procesado el trazo.

### <a name="special-considerations"></a>Consideraciones especiales

En la lista siguiente se describen otros puntos que se deben tener en cuenta al usar el objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) .

-   No debe adjuntar un objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a más de un objeto [**RealTimeStylus**](realtimestylus-class.md) . Una vez que se habilitan dos objetos **RealTimeStylus** a los que está asociado el objeto **DynamicRenderer** , ocurre lo siguiente.

    -   El objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) produce una excepción en respuesta a la segunda llamada a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) .
    -   El segundo objeto [**RealTimeStylus**](realtimestylus-class.md) que se ha habilitado genera un objeto de [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) y notifica los complementos restantes en sus colecciones de complementos del error.
    -   El objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) deja de representar los datos del lápiz de Tablet PC.

-   El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción cuando se llama a su método [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) con el parámetro *GUID* establecido en el identificador único global (GUID) de DynamicRendererCachedDataGuid.
-   El objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) se implementa como un contenedor com (modelo de objetos componentes) y no se puede llamar directamente a sus métodos de la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Para obtener más información sobre la operación COM y el objeto [**RealTimeStylus**](realtimestylus-class.md) , consulte [las notas de implementación de las API de StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Representación personalizada

Puede crear su propio complemento de representador dinámico mediante la creación de un complemento sincrónico que se suscribe a las notificaciones [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**paquetes**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)y [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) . A continuación, el complemento puede representar el trazo mientras se dibuja. Puede tratarse de una manera de implementar una herramienta de selección que use un cuadro de selección o selección de forma libre, por ejemplo.

 

 
