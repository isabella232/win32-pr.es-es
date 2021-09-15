---
title: Uso del control Reproductor de Windows Media con Visual Basic
description: Uso del control Reproductor de Windows Media con Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móviles, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,Visual Basic
- Reproductor de Windows Media modelo de objetos, Visual Basic
- modelo de objetos, Visual Basic
- Reproductor de Windows Media Móvil, Visual Basic
- Reproductor de Windows Media ActiveX control, Visual Basic
- Reproductor de Windows Media Control ActiveX móvil, Visual Basic
- ActiveX control, Visual Basic
- Visual Basic la inserción de programas basados en archivos
- inserción, Visual Basic basados en aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359876"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>Uso del control Reproductor de Windows Media con Visual Basic

En esta sección se describe cómo usar el control Reproductor de Windows Media serie 9 o posterior ActiveX en aplicaciones creadas con Microsoft Visual Basic 6.0.

## <a name="getting-started"></a>Introducción

Para agregar el control Reproductor de Windows Media al cuadro  de herramientas, seleccione componentes en el **menú Project** herramientas. En el cuadro de diálogo Componentes, active la casilla situada junto a "Reproductor de Windows Media". En la parte inferior del cuadro de diálogo, confirme que el archivo seleccionado está wmp.dll. Después de cerrar el cuadro de diálogo, puede colocar una instancia del control Reproductor de Windows Media en el formulario de las maneras habituales.

Puede establecer muchas propiedades de control mediante el ventana Propiedades. Para establecer algunas propiedades, debe usar el cuadro de diálogo Reproductor de Windows Media propiedades, que se abre mediante el elemento "(Custom)" de la ventana Propiedades.

## <a name="object-references"></a>Referencias a objetos

Se usan determinadas propiedades del control Player para obtener referencias a objetos concretos. Por ejemplo, la **propiedad cdromCollection** devuelve una referencia a un **objeto CdromCollection.** Debe asignar dicha referencia a una variable que declaró como la interfaz correspondiente. En el caso de la **propiedad cdromCollection,** por ejemplo, se asigna su valor devuelto a una variable de tipo **IWMPCdromCollection**.

Lea el [tema Interfaces en](interfaces.md) referencia del modelo de [objetos para C++](object-model-reference-for-c.md) para identificar qué objetos implementan varias interfaces. En esos casos, debe declarar una variable de objeto como la interfaz numerada más alta documentada en este SDK para tener acceso a todas las propiedades y métodos de ese objeto. Por ejemplo, debe asignar el valor de la propiedad **currentMedia** del control Reproductor de Windows Media a una variable declarada como **IWMPMedia3** para asegurarse de que tiene acceso a los métodos **getAttributeCountByType** y **getItemInfoByType.**

> [!Note]  
> El objeto **WindowsMediaPlayer** implementa todas las propiedades y métodos de las interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3,** **IWMPPlayer,** **IWMPPlayer2,** **IWMPPlayer3** e **IWMPPlayer4.** No es necesario declarar variables independientes para ninguna de estas interfaces. Puede acceder a todos sus miembros con el nombre que asignó a la **instancia de WindowsMediaPlayer.**

 

En el Visual Basic object browser verá muchas interfaces diseñadas para uso privado por el control Reproductor de Windows Media, incluidas algunas que admiten desarrolladores de máscaras. Solo debe usar los objetos, propiedades, métodos y eventos que se documentan en este SDK.

## <a name="additional-tips"></a>Consejos adicionales

-   La documentación de referencia muestra JScript sintaxis. En JScript, los argumentos pasados a los métodos siempre se incluyen entre paréntesis. En Visual Basic 6.0, los argumentos pasados a métodos que no devuelven un valor no se deben incluir entre paréntesis.
-   Es posible que algunas propiedades o métodos no aparezcan en la característica Finalización de código de la lista automática en Visual Basic editor de código. Puede seguir utilizando esos miembros escribiendo sus nombres exactamente como aparecen en esta documentación.
-   Administre la apariencia visual del control mediante la **propiedad uimode.** Puede hacerlo de dos maneras. Puede usar **la** lista desplegable Seleccionar un modo en el cuadro de diálogo Reproductor de Windows Media Propiedades o puede escribir el valor correcto en la ventana Propiedades.

    En concreto, no use la **propiedad visible** para ocultar el control; en su lugar, asigne el valor "invisible" a la **propiedad uimode.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control de reproductor**](player-control-guide.md)
</dt> </dl>

 

 




