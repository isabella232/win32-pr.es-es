---
title: Uso del control Reproductor de Windows Media con Microsoft Office
description: Uso del control Reproductor de Windows Media con Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,Office
- Reproductor de Windows Media modelo de objetos, Office
- modelo de objetos, Office
- Reproductor de Windows Media Móvil, Office
- Reproductor de Windows Media ActiveX control, Office
- Reproductor de Windows Media Control ActiveX móvil, Office
- ActiveX control, Office
- Office inserción de documentos
- inserción, Office documentos
- Reproductor de Windows Media ActiveX control, Excel
- Reproductor de Windows Media Control ActiveX móvil, Excel
- ActiveX control, Excel
- embedding,Excel hojas de cálculo
- Excel inserción de hojas de cálculo
- Reproductor de Windows Media ActiveX control, PowerPoint
- Reproductor de Windows Media Control ActiveX móvil, PowerPoint
- ActiveX control, PowerPoint
- inserción, PowerPoint diapositivas
- PowerPoint inserción de diapositivas
- Reproductor de Windows Media ActiveX control, Word
- Reproductor de Windows Media Control de ActiveX móvil, Word
- ActiveX control, Word
- Inserción de documentos de Word
- embedding,Word documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418c082cad2793e3ebd676c4d648339f9e637f46c7519efc1b426a44b69ee05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001405"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Uso del control Reproductor de Windows Media con Microsoft Office

En esta sección se describe cómo insertar el control Reproductor de Windows Media serie 9 o posterior ActiveX en varios documentos creados mediante Microsoft Office XP.

En Microsoft Word, Excel y PowerPoint®, para insertar el control, seleccione Objeto  en  el menú Insertar y, a continuación, elija **Reproductor de Windows Media** en la lista de tipos de objetos disponibles. El Reproductor de Windows Media aparece en el documento en la ubicación actual. A continuación, puede seleccionar **Control** de formato **(Objeto** de formato en Excel) en el menú contextual del control para ajustar el diseño, el estilo de ajuste de texto y otras opciones de formato. En Word Excel, debe estar en modo de diseño para ello.

Una vez que haya situado y formatado el  control, puede configurarlo mediante el cuadro de diálogo Propiedades, al que se puede acceder desde el Cuadro de herramientas de **control** o desde el menú contextual en modo de diseño para Word y Excel. Aquí puede especificar propiedades básicas del control Player, como el nombre del control, la dirección URL de un archivo multimedia digital y el modo de interfaz de usuario. Establecer la propiedad **uiMode** en "none" oculta todo el contenido del control excepto la ventana de vídeo o visualización, lo que le permite agregar sus propios botones y escribir código de script mediante Visual Basic para Aplicaciones (VBA) para controlar los clics de botón y los eventos de control player.

Desde el  cuadro de diálogo Propiedades básicas, también puede acceder al cuadro de diálogo Propiedades de control de **Reproductor de Windows Media** más sofisticado haciendo doble clic en la fila "(Custom)" o haciendo clic en el botón de puntos suspensivos ("...") después de seleccionar esa fila. En este cuadro de diálogo, puede modificar todas las propiedades de control Player disponibles.

> [!Note]  
> Debe tener cuidado de no realizar acciones en controladores de eventos de control player que darán lugar a la destrucción del control. Por ejemplo, si inserta el control Reproductor de Windows Media en una diapositiva de una presentación de PowerPoint, no llame al método PowerPoint **Next** desde el evento **Player openStateChange** ni ningún otro evento.

 

> [!Note]  
> Además, no debe establecer la propiedad **Player.URL** desde un controlador de eventos de control Player.

 

En FrontPage, agregue el control Reproductor de Windows Media a una página web seleccionando **Componente web** en el **menú** Insertar. En el cuadro **de diálogo** Insertar componente  web , seleccione **Controles** avanzados en la lista Tipo de componente y, a continuación, **seleccione ActiveX Control** en la lista de opciones de control. En la ventana siguiente del cuadro de diálogo, **seleccione Reproductor de Windows Media**. Si no aparece, haga clic en **Personalizar** y active **Reproductor de Windows Media** en la **lista Control** .

Una vez insertado Reproductor de Windows Media control, puede colocarlo y cambiar su tamaño, y modificar sus propiedades seleccionando ActiveX **Propiedades del control** en el menú contextual del control. En la vista HTML, los valores de propiedad que especifique aparecen en el elemento OBJECT que representa Reproductor de Windows Media control. El nombre del objeto aparece como el atributo ID y las propiedades del control aparecen como etiquetas PARAM. El nombre del objeto proporciona acceso al modelo de objetos Reproductor de Windows Media control, que puede programar mediante Microsoft JScript. Para obtener más información, [vea Using the Reproductor de Windows Media Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control de reproductor**](player-control-guide.md)
</dt> </dl>

 

 




