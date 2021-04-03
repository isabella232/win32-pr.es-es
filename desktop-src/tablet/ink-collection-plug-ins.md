---
description: El objeto RealTimeStylus no recopila de forma inherente la tinta. Para usar RealTimeStylus para recopilar la entrada manuscrita, cree un complemento de recopilador de tinta.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Complementos de Ink-Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907715"
---
# <a name="ink-collection-plug-ins"></a>Complementos de Ink-Collection

El objeto [**RealTimeStylus**](realtimestylus-class.md) no recopila de forma inherente la tinta. Para usar **RealTimeStylus** para recopilar la entrada manuscrita, cree un complemento de recopilador de tinta.

A continuación se indica un escenario mínimo para usar el objeto [**RealTimeStylus**](realtimestylus-class.md) en un formulario que recopila entradas manuscritas.

1.  Cree un formulario que implemente la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Cree un objeto [**RealTimeStylus**](realtimestylus-class.md) y asócielo a un control en el formulario.
3.  Establezca interés en las notificaciones StylusDown, packets y StylusUp en la propiedad [Interest](/previous-versions/ms574886(v=vs.100)) del formulario.
4.  En los métodos [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)y [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del formulario, agregue código para controlar el lápiz hacia abajo, los paquetes y las notificaciones del lápiz óptico que se envían desde el objeto [**RealTimeStylus**](realtimestylus-class.md) del formulario. Este código debe almacenar los datos de lápiz y crear y almacenar los trazos.

Para obtener un ejemplo de este tipo de aplicación, vea el ejemplo de ejemplo de [colección de tintas RealTimeStylus](realtimestylus-ink-collection-sample.md) .

> [!Note]  
> Cuando se produce un evento [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) , llame al método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de los trazos recopilados en un controlador de eventos DisplaySettingsChanged para volver a calcular las propiedades de [ancho](/previous-versions/ms582112(v=vs.100)) y [alto](/previous-versions/ms582106(v=vs.100)) . Esto es necesario para tener en cuenta los posibles cambios de puntos por pulgada (PPP) que son el resultado del evento DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Recopilación y reconocedores de tinta

Ni el análisis de tinta ni el reconocimiento de escritura a mano es una función del objeto [**RealTimeStylus**](realtimestylus-class.md) . Como el complemento del recopilador de tintas recopila tinta o como desea reconocer la tinta, puede copiar la tinta en un objeto [RecognizerContext](/previous-versions/ms552546(v=vs.100)) o [divisor](/previous-versions/ms583616(v=vs.100)) . Para obtener más información sobre el reconocimiento y el análisis de tinta, consulte [acerca del reconocimiento de escritura a mano](about-handwriting-recognition.md) o [el objeto divisor](the-divider-object.md).

## <a name="static-rendering"></a>Representación estática

Para representar la entrada de lápiz mientras se está recopilando, adjunte un objeto [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) al objeto [**RealTimeStylus**](realtimestylus-class.md) . Para representar la entrada de lápiz una vez recopilada, utilice un objeto de [representador](/previous-versions/ms552630(v=vs.100)) para dibujar los trazos en el objeto de [gráficos](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) adecuado. Para obtener más información sobre el objeto DynamicRenderer, vea [Complementos de representador dinámico](dynamic-renderer-plug-ins.md). Para obtener un ejemplo de la representación estática y dinámica, vea [ejemplo de colección de tintas RealTimeStylus](realtimestylus-ink-collection-sample.md).

 

 
