---
description: Información general sobre las consideraciones para diseñar una aplicación que usa las interfaces de programación de aplicaciones (API) de StylusInput.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Consideraciones de diseño para la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff526d8e073f00156730d79ea2caf1a02c5e5af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361336"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Consideraciones de diseño para la API de StylusInput

Las siguientes son consideraciones de diseño para la API de StylusInput.

-   Puede actualizar la propiedad [**WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) del objeto [**RealTimeStylus**](realtimestylus-class.md) y la propiedad [**ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) del objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) mientras el lápiz está inactivo. Esto puede ser útil si desea tener un área de dibujo dinámica mientras la aplicación está recopilando entradas manuscritas.
-   Para optimizar la reutilización y el mantenimiento del código de complemento, los complementos no deben realizar llamadas directamente a la aplicación, sino que deben usar el objeto [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) ([CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) en código administrado) para comunicarse con la aplicación.
-   Las colecciones de complementos del objeto [**RealTimeStylus**](realtimestylus-class.md) están ordenadas. La posición relativa de los complementos dentro de estas colecciones puede ser muy importante. Por ejemplo, un complemento que modifica la información de paquetes debe agregarse probablemente a la colección de complementos sincrónicos antes de un complemento de representador dinámico.
-   La capacidad de agregar datos de lápiz personalizados al flujo de datos del lápiz de Tablet PC debe usarse con moderación. Use esta característica solo si otro complemento necesita recibir esta información como parte del flujo de datos. Además, evite agregar datos de lápiz personalizados en respuesta a otros datos de lápiz personalizados que entran en el complemento, ya que esto puede crear un bucle infinito.
-   Las colecciones de complementos se pueden modificar mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado; sin embargo, esto puede dificultar el comportamiento de la aplicación. Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama a Microsoft. StylusInput. IStylusSyncPlugin del complemento. Método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) (el método [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) en código administrado). Cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) del complemento ( [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) o el método [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) en código administrado). Esto permite que el complemento mantenga su estado adecuado sin tener que comprobar la propiedad [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) del objeto **RealTimeStylus** . Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, es posible que los datos del complemento que recibe el complemento no contengan suficiente información para establecer adecuadamente el contexto de los datos iniciales. Por ejemplo, el complemento que se acaba de agregar podría empezar a recibir datos de paquetes de un lápiz que es un trazo medio. Del mismo modo, cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, los datos del complemento que ha recibido el complemento pueden ser insuficientes para finalizar el procesamiento de los datos.
    > [!Note]  
    > Para la estabilidad general, restablezca el estado interno de un complemento cuando se llame a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .

     

-   El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento modifica la colección de complementos a la que está adjuntada. Esto solo ocurre cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama como miembro de esa colección.

 

 
