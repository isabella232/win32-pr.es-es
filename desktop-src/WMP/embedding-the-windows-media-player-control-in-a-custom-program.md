---
title: Incrustar el control Media Player de Windows en un programa personalizado
description: Incrustar el control Media Player de Windows en un programa personalizado
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Windows Media Player Mobile, incrustar el control ActiveX
- incrustación, programas personalizados
- incrustación de programas personalizados
- incrustación, programas basados en Visual Basic
- Incrustación de programas basados en Visual Basic
- incrustar, usar manualmente métodos COM
- incrustación manual mediante métodos COM
- incrustación, programas de C++
- Incrustación de programas de C++
- incrustación, programas de Visual Studio
- Visual Studio, inserción de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075498"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>Incrustar el control Media Player de Windows en un programa personalizado

Dado que el control ActiveX de Windows Media Player se basa en la tecnología del modelo de objetos componentes (COM) de Microsoft, puede incrustarlo en programas escritos con muchos lenguajes de programación diferentes. El control Media Player de Windows representa una manera fácil de agregar sofisticada funcionalidad multimedia digital a cualquier programa.

En Microsoft Visual Basic, puede Agregar el control al cuadro de herramientas de control, colocarlo en un formulario y ajustar las propiedades del control en la ventana Propiedades. Si desea una interfaz de usuario personalizada, puede colocar botones de comando en el formulario y agregar el código que administra el control de Media Player de Windows. Incrustar el control en un programa basado en Visual Basic es muy similar a insertarlo en un documento de Office y programarlo con VBA.

Como alternativa, puede incrustar el control manualmente mediante métodos COM para crear instancias del control y tener acceso a las interfaces COM documentadas en [Referencia del modelo de objetos para C++](object-model-reference-for-c.md).

Al incrustar el control Media Player de Windows en un programa de C++, tiene la opción de implementar interfaces COM que permiten que el control se ejecute en modo remoto. Esto significa que el control incrustado comparte el mismo motor de reproducción que el modo completo del reproductor y los usuarios pueden alternar entre el modo completo y el estado acoplado sin interrumpir la reproducción de medios digitales. También puede controlar lo que se muestra en los distintos paneles del reproductor en modo completo cuando los usuarios cambian al estado desacoplado.

Con la incrustación de C++, también tiene la opción de aplicar un archivo de definición de máscara al control Embedded Player. Se trata de una forma sencilla de crear un código de interfaz de usuario ligero que se puede mantener por separado del código de programa principal.

Microsoft Visual Studio admite la incrustación de controles ActiveX, incluido el control de Media Player de Windows. Cuando elige hacer esto, Visual Studio crea un nuevo ensamblado de interoperabilidad alternativo (Interop) para administrar la interoperabilidad entre el .NET Framework y el control de Media Player de Windows. Visual Studio usa la herramienta de tlbimp.exe de .NET Framework para crear el ensamblado de interoperabilidad. Esto significa que las firmas que se muestran al usar la característica IntelliSense en Visual Studio usan la semántica determinada por la versión actual de Tlbimp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Incrustar el control Media Player de Windows**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**Usar el control Media Player de Windows en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**Usar el control de Media Player de Windows en una solución de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Usar el control Media Player de Windows con Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




