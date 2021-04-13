---
title: Usar el control Media Player de Windows con Visual Basic
description: Usar el control Media Player de Windows con Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Media Player de Windows, Visual Basic
- Modelo de objetos de Windows Media Player, Visual Basic
- modelo de objetos, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Control ActiveX de Windows Media Player, Visual Basic
- Control ActiveX de Windows Media Player Mobile, Visual Basic
- Control ActiveX, Visual Basic
- Incrustación de programas basados en Visual Basic
- incrustación, programas basados en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357312"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>Usar el control Media Player de Windows con Visual Basic

En esta sección se describe cómo usar la serie Windows Media Player 9 o el control ActiveX posterior en aplicaciones creadas con Microsoft Visual Basic 6,0.

## <a name="getting-started"></a>Introducción

Para agregar el control Media Player de Windows al cuadro de herramientas, primero seleccione **componentes** en el menú **proyecto** . En el cuadro de diálogo componentes, active la casilla situada junto a "Windows Media Player". En la parte inferior del cuadro de diálogo, confirme que el archivo seleccionado está wmp.dll. Después de cerrar el cuadro de diálogo, puede colocar una instancia del control Media Player de Windows en el formulario de la manera habitual.

Puede establecer muchas propiedades de control mediante el ventana Propiedades. Para establecer algunas propiedades, debe usar el cuadro de diálogo Propiedades de Media Player de Windows, que se abre con el elemento "(personalizado)" en el ventana Propiedades.

## <a name="object-references"></a>Referencias a objetos

Puede usar ciertas propiedades de control del reproductor para obtener referencias a objetos concretos. Por ejemplo, la propiedad **cdromCollection** devuelve una referencia a un objeto **cdromCollection** . Debe asignar este tipo de referencia a una variable que declaró como la interfaz correspondiente. Por ejemplo, en el caso de la propiedad **cdromCollection** , se asigna el valor devuelto a una variable de tipo **IWMPCdromCollection**.

Lea el tema [interfaces](interfaces.md) en la [Referencia del modelo de objetos de C++](object-model-reference-for-c.md) para identificar qué objetos implementan varias interfaces. En esos casos, debe declarar una variable de objeto como la interfaz con el número más alto documentada en este SDK para tener acceso a todas las propiedades y los métodos de ese objeto. Por ejemplo, debe asignar el valor de la propiedad **currentMedia** de control de Windows Media Player a una variable declarada como **IWMPMedia3** para asegurarse de que tiene acceso a los métodos **getAttributeCountByType** y **getItemInfoByType** .

> [!Note]  
> El objeto **WindowsMediaPlayer** implementa todas las propiedades y los métodos de las interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** y **IWMPPlayer4** . No es necesario declarar variables independientes para cualquiera de estas interfaces. Puede tener acceso a todos sus miembros mediante el nombre que asignó a la instancia de **WindowsMediaPlayer** .

 

En el Visual Basic Examinador de objetos verá muchas interfaces que están destinadas al uso privado del control de Media Player de Windows, incluidos algunos que admiten desarrolladores de máscaras. Solo debe usar los objetos, las propiedades, los métodos y los eventos que se documentan en este SDK.

## <a name="additional-tips"></a>Consejos adicionales

-   La documentación de referencia muestra la sintaxis de JScript. En JScript, los argumentos pasados a los métodos siempre se incluyen entre paréntesis. En Visual Basic 6,0, los argumentos pasados a métodos que no devuelven un valor no se deben incluir entre paréntesis.
-   Es posible que algunas propiedades o métodos no aparezcan en la característica lista automática de finalización de código en el editor de código de Visual Basic. Puede seguir usando estos miembros escribiendo sus nombres exactamente como aparecen en esta documentación.
-   Administrar la apariencia visual del control mediante la propiedad **uiMode** . Puede hacerlo de dos maneras. Puede usar la lista desplegable **seleccionar un modo** del cuadro de diálogo Propiedades de Windows Media Player, o bien puede escribir el valor correcto en el ventana Propiedades.

    En concreto, no utilice la propiedad **visible** para ocultar el control; en su lugar, asigne el valor "invisible" a la propiedad **uiMode** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> </dl>

 

 




