---
description: Un complemento de representador dinámico es un objeto que muestra los datos del lápiz de tableta en tiempo real a medida que lo controla el objeto RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Dynamic-Renderer complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6426dfc9f1dae8561802d2cf6c5613fb786600504cc8600046c4df781239abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092691"
---
# <a name="dynamic-renderer-plug-ins"></a>Dynamic-Renderer complementos

Un complemento de representador dinámico es un objeto que muestra los datos del lápiz de tableta en tiempo real a medida que lo controla el objeto [**RealTimeStylus.**](realtimestylus-class.md) Más adelante, para eventos como una actualización de formulario, el complemento de representador dinámico o un complemento de recopilador de lápiz pueden volver a dibujar la entrada de lápiz.

## <a name="the-dynamicrenderer-object"></a>El objeto DynamicRenderer

El [**objeto RealTimeStylus**](realtimestylus-class.md) implementa la [**interfaz IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) El [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) representa la entrada de lápiz en tiempo real, a medida que se dibuja. Cuando se [**llama al método Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) mientras el objeto **DynamicRenderer** está habilitado, el objeto **DynamicRenderer** vuelve a dibujar el trazo que se está recopilando actualmente. La propiedad Enabled [](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) del objeto **DynamicRenderer** se establece inicialmente en **FALSE.**

> [!Note]  
> Al llamar al método [**Refresh**](/previous-versions/ms826370(v=msdn.10)) del objeto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) desde un controlador de eventos de Paint en código administrado, establezca la propiedad [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10)) del objeto **DynamicRenderer** [en](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) la propiedad [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) del objeto [PaintEventArgs.](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1)

 

El [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) puede almacenar temporalmente en caché los datos de entrada de lápiz. Para usar esta característica en código administrado, establezca la [propiedad EnableDataCache](/previous-versions/ms826349(v=msdn.10)) en **TRUE.** Cuando el objeto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) recibe una llamada a su método [**IStylusSyncPlugin.StylusUp,**](/previous-versions/ms826366(v=msdn.10)) almacena en caché los datos del trazo y agrega datos de lápiz óptico personalizados a la cola input en respuesta al objeto [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) del trazo. La propiedad [CustomDataId](/previous-versions/ms824749(v=msdn.10)) del objeto [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) se establece en el valor [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) y la propiedad Data del objeto **CustomStylusData** contiene un objeto DynamicRendererCachedData. Llame al método [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) del objeto **DynamicRenderer** una vez recopilado el trazo y se pueda representar estáticamente. Cuando se [**llama al método Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) mientras el objeto **DynamicRenderer** está habilitado, el objeto **DynamicRenderer** vuelve a dibujar todos los trazos almacenados en caché. Cuando la [**propiedad DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) se establece en **false,** se eliminan los datos del trazo almacenados en caché.

En el diagrama siguiente se muestra cómo el objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) agrega datos a los datos del lápiz de tableta cuando se establece la [**propiedad DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) del objeto **DynamicRenderer.**

![ilustración que muestra el flujo de datos del representador dinámico](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

En este diagrama, el círculo con la letra "SD" representa un objeto [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) y los círculos con la letra "P" representan objetos [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con letras "SU" representa un [**objeto StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y, a continuación, se coloca en la cola de salida. Los círculos con la letra "DR" representan datos de lápiz óptico personalizados que el complemento [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) agrega a la cola de entrada en respuesta a la notificación de lápiz óptico asociada a "SU". A continuación, los datos del lápiz óptico personalizados con la letra "DR" se pasan a los complementos sincrónicos y, a continuación, a la cola de salida antes de que se procese el siguiente lápiz de tableta. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta. También se representa en el diagrama el complemento del recopilador de entrada de lápiz que llama al método [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) del objeto **DynamicRenderer** para liberar los datos del trazo almacenados en caché después de que el complemento de colección de lápiz haya procesado el trazo.

### <a name="special-considerations"></a>Consideraciones especiales

En la lista siguiente se describen otros puntos que se deben tener en cuenta al usar el [**objeto DynamicRenderer.**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))

-   No debe adjuntar un [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a más de un [**objeto RealTimeStylus.**](realtimestylus-class.md) Una vez que se habilitan dos objetos **RealTimeStylus** a los que está asociado el objeto **DynamicRenderer,** se produce lo siguiente.

    -   El [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) produce una excepción en respuesta a la segunda llamada a su [**método RealTimeStylusEnabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled)
    -   El segundo [**objeto RealTimeStylus**](realtimestylus-class.md) habilitado genera un objeto [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) y notifica el error a los complementos restantes en sus colecciones de complementos.
    -   El [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) deja de representar datos de lápiz de tableta.

-   El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción cuando se llama a su [**método AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) con el parámetro *guid* establecido en el identificador único global (GUID) DynamicRendererCachedDataGuid.
-   El [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) se implementa como un contenedor de Modelo de objetos componentes (COM) y no se puede llamar directamente a sus métodos de interfaz [**IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) Para obtener más información sobre la operación COM y el [**objeto RealTimeStylus,**](realtimestylus-class.md) vea Notas de [implementación de las API StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Representación personalizada

Puede crear su propio complemento de representador dinámico mediante la creación de un complemento sincrónico que se suscribe a las notificaciones [**StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)y [**StylusUp.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) A continuación, el complemento puede representar el trazo mientras se dibuja. Esta puede ser una manera de implementar una herramienta de selección que use un cuadro de selección o selección de forma libre, por ejemplo.

 

 
