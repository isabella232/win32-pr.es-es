---
description: Información general sobre las consideraciones para diseñar una aplicación que usa las interfaces de programación de aplicaciones (API) StylusInput.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Consideraciones de diseño para StylusInput API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd97a5bad203dd23611acf3d6cb07bead1e1744a10b9ac39afe8a53e65597d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936635"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Consideraciones de diseño para StylusInput API

A continuación se describen las consideraciones de diseño para StylusInput API.

-   Puede actualizar la propiedad [**WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) del objeto [**RealTimeStylus**](realtimestylus-class.md) y la [**propiedad ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) del objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) mientras el lápiz está fuera de servicio. Esto puede ser útil cuando se desea tener un área de dibujo dinámico mientras la aplicación recopila entrada de lápiz.
-   Para optimizar la reutilización y el mantenimiento del código del complemento, los complementos no deben realizar llamadas directamente a la aplicación, sino que deben usar el objeto [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) [(CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) en código administrado) para comunicarse con la aplicación.
-   Se ordenan las colecciones de complementos del objeto [**RealTimeStylus.**](realtimestylus-class.md) La posición relativa de los complementos dentro de estas colecciones puede ser muy importante. Por ejemplo, un complemento que modifica la información de paquetes probablemente se debe agregar a la colección de complementos sincrónicos antes de un complemento de representador dinámico.
-   La capacidad de agregar datos de lápiz óptico personalizados al flujo de datos del lápiz de tableta debe usarse con moderación. Use esta característica solo si otro complemento necesita recibir esta información como parte del flujo de datos. Además, evite agregar datos de lápiz óptico personalizados en respuesta a otros datos de lápiz personalizados que se incluyen en el complemento, ya que esto puede crear un bucle infinito.
-   Las colecciones de complementos se pueden modificar mientras el [**objeto RealTimeStylus**](realtimestylus-class.md) está habilitado; sin embargo, esto puede dificultar la predicción del comportamiento de la aplicación. Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama a Microsoft.StylusInput.IStylusSyncPlugin del complemento. Método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) (el método [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusEnabled en](/previous-versions/ms824775(v=msdn.10)) código administrado). Cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) del complemento (ya sea el método [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) en código administrado). Esto permite que el complemento mantenga su estado adecuado sin tener que comprobar la propiedad [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) del **objeto RealTimeStylus.** Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, es posible que los datos de complemento que recibe el complemento no contengan suficiente información para establecer adecuadamente el contexto de los datos iniciales. Por ejemplo, el complemento recién agregado podría empezar a recibir datos de paquetes de un lápiz que es de trazo medio. De forma similar, cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, los datos del complemento que ha recibido el complemento pueden ser insuficientes para terminar de procesar los datos.
    > [!Note]  
    > Para una estabilidad general, restablezca el estado interno de un complemento cuando se llame a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled)

     

-   El [**objeto RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento modifica la colección de complementos a la que está asociado. Esto solo sucede cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama como miembro de esa colección.

 

 
