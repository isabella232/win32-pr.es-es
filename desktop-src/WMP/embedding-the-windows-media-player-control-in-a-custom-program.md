---
title: Insertar el control Reproductor de Windows Media en un programa personalizado
description: Insertar el control Reproductor de Windows Media en un programa personalizado
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móviles, inserción
- Reproductor de Windows Media Mobile,embedding ActiveX control
- embedding,custom programs
- inserción de programas personalizados
- inserción, Visual Basic basados en aplicaciones
- Visual Basic la inserción de programas basada en archivos
- inserción, uso manual de métodos COM
- inserción manual mediante métodos COM
- inserción, programas de C++
- Inserción de programas de C++
- embedding,Visual Studio programas
- Visual Studio, inserción de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b700f1ad4609f36750148c90ab26661498a0cc6186dba2928e90bcec9e63bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863005"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>Insertar el control Reproductor de Windows Media en un programa personalizado

Dado que Reproductor de Windows Media ActiveX control se basa en la tecnología del Modelo de objetos componentes (COM) de Microsoft, puede insertarlo en programas escritos con muchos lenguajes de programación diferentes. El Reproductor de Windows Media control representa una manera sencilla de agregar una funcionalidad multimedia digital sofisticada a cualquier programa.

En Microsoft Visual Basic, puede agregar el control al cuadro de herramientas del control, colocarlo en un formulario y ajustar las propiedades del control en la ventana de propiedades. Si desea una interfaz de usuario personalizada, puede colocar botones de comando en el formulario y agregar código que administre el control Reproductor de Windows Media usuario. Insertar el control en un programa basado en Visual Basic es muy similar a insertarlo en un documento Office y programarlo con VBA.

Como alternativa, puede insertar manualmente el control mediante métodos COM para crear instancias del control y acceder a las interfaces COM documentadas en Referencia del modelo de objetos [para C++.](object-model-reference-for-c.md)

Al insertar el control Reproductor de Windows Media en un programa de C++, tiene la opción de implementar interfaces COM que permiten que el control se ejecute en modo remoto. Esto significa que el control incrustado comparte el mismo motor de reproducción que el modo completo del reproductor, y los usuarios pueden cambiar entre el modo completo y el estado acoplado sin interrumpir la reproducción de medios digitales. También puede controlar lo que se muestra en los distintos paneles del reproductor en modo completo cuando los usuarios cambian al estado desacoplado.

Con la inserción de C++, también tiene la opción de aplicar un archivo de definición de máscara al control Player insertado. Esta es una manera sencilla de crear código ligero de interfaz de usuario que puede mantener por separado del código del programa principal.

Microsoft Visual Studio permite insertar controles ActiveX, incluido el control Reproductor de Windows Media control . Cuando decida hacerlo, Visual Studio un nuevo ensamblado de interoperabilidad alternativo (interoperabilidad) para administrar la interoperabilidad entre el .NET Framework y el control Reproductor de Windows Media. Visual Studio usa la herramienta .NET Framework tlbimp.exe para crear el ensamblado de interoperabilidad. Esto significa que las firmas que se muestran al usar la característica IntelliSense en Visual Studio usan semántica determinada por la versión actual de tlbimp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Inserción del control Reproductor de Windows Media control**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en una solución .NET Framework de datos**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Uso del control Reproductor de Windows Media con Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




