---
title: Usar el control Media Player de Windows con Microsoft Office
description: Usar el control Media Player de Windows con Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, Office
- Modelo de objetos de Windows Media Player, Office
- modelo de objetos, Office
- Windows Media Player Mobile, Office
- Windows Media Player control ActiveX, Office
- Control ActiveX móvil de Windows Media Player, Office
- Control ActiveX, Office
- Incrustación de documentos de Office
- incrustación, documentos de Office
- Control ActiveX de Windows Media Player, Excel
- Control ActiveX móvil de Windows Media Player, Excel
- Control ActiveX, Excel
- incrustación, hojas de cálculo de Excel
- Incrustación de hojas de cálculo de Excel
- Control ActiveX de Windows Media Player, PowerPoint
- Control ActiveX móvil de Windows Media Player, PowerPoint
- Control ActiveX, PowerPoint
- incrustación, presentaciones de diapositivas de PowerPoint
- Incrustación de diapositivas de PowerPoint
- Windows Media Player control ActiveX, Word
- Control ActiveX móvil de Windows Media Player, Word
- Control ActiveX, Word
- Incrustación de documentos de Word
- incrustación, documentos de Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994288"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Usar el control Media Player de Windows con Microsoft Office

En esta sección se describe cómo insertar la serie Windows Media Player 9 o un control ActiveX posterior en varios documentos creados con Microsoft Office XP.

En Microsoft Word, Excel y PowerPoint®, para incrustar el control, seleccione **objeto** en el menú **Insertar** y, a continuación, elija **Media Player de Windows** en la lista de tipos de objeto disponibles. El control Media Player de Windows aparece en el documento en la ubicación actual. A continuación, puede seleccionar el **control de formato** ( **objeto de formato** en Excel) en el menú contextual del control para ajustar el diseño, el estilo de ajuste de texto y otras opciones de formato. En Word y Excel, debe estar en modo de diseño para hacerlo.

Una vez que haya colocado y formateado el control, puede configurarlo mediante el cuadro de diálogo **propiedades** , al que se puede tener acceso desde el cuadro de **herramientas de control** o desde el menú contextual en modo de diseño para Word y Excel. Aquí puede especificar propiedades básicas del control Player, como el nombre del control, la dirección URL de un archivo multimedia digital y el modo de interfaz de usuario. Al establecer la propiedad **uiMode** en "none", se oculta todo el control, excepto el vídeo o la ventana de visualización, lo que le permite agregar sus propios botones y escribir código de script mediante Visual Basic para aplicaciones (VBA) para controlar los clics de botón y los eventos de control de reproductor.

En el cuadro de diálogo **propiedades** básicas, también puede tener acceso al cuadro de diálogo **propiedades de Control de Windows Media Player** más sofisticadas haciendo doble clic en la fila "(personalizada)" o haciendo clic en el botón de puntos suspensivos ("...") después de seleccionar esa fila. En este cuadro de diálogo, puede modificar todas las propiedades de control del reproductor disponibles.

> [!Note]  
> Debe tener cuidado de no tomar medidas en los controladores de eventos de control de reproductor que provocarán que el control se destruya. Por ejemplo, si incrusta el control Media Player de Windows en una diapositiva de una presentación de PowerPoint, no llame al método **Next** de PowerPoint desde el evento Player **openStateChange** o cualquier otro evento.

 

> [!Note]  
> Además, no debe establecer la propiedad **Player. URL** desde un controlador de eventos de control de reproductor.

 

En FrontPage, agregue el control Media Player de Windows a una página web seleccionando **componente web** en el menú **Insertar** . En el cuadro de diálogo **Insertar componente web** , seleccione **controles avanzados** en la lista **tipo de componente** y, a continuación, seleccione **control ActiveX** en la lista de opciones de control. En la siguiente ventana del cuadro de diálogo, seleccione **Windows Media Player**. Si no aparece, haga clic en **personalizar** y active la casilla **Media Player de Windows** en la lista de **controles** .

Una vez incrustado el control de Media Player de Windows, puede colocarlo y cambiar su tamaño, y modificar sus propiedades seleccionando **propiedades de controles ActiveX** en el menú contextual del control. En la vista HTML, los valores de propiedad que especifique aparecen en el elemento de objeto que representa el control de Media Player de Windows. El nombre del objeto aparece como el atributo ID y las propiedades del control aparecen como etiquetas PARAM. El nombre de objeto proporciona acceso al modelo de objetos de control de Media Player de Windows, que puede programar con Microsoft JScript. Para obtener más información, vea [usar el Control Media Player de Windows en una página web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> </dl>

 

 




