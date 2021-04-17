---
description: En este tema se describe cómo ajustar imágenes mediante la propiedad System. Windows. Forms. PictureBox. SizeMode y cómo mostrar imágenes en Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Trabajar con imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696593"
---
# <a name="working-with-pictures"></a>Trabajar con imágenes

En este tema se describe cómo ajustar imágenes mediante la propiedad [System. Windows. Forms. PictureBox. SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) y cómo mostrar imágenes en Microsoft Visual Studio .net.

## <a name="the-sizemode-property"></a>La propiedad SizeMode

Puede especificar cómo encaja una imagen en el control con la propiedad [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) . La propiedad SizeMode está disponible en la biblioteca administrada y en la biblioteca de Automation. Con SizeMode puede:

-   Cambiar el tamaño de los bordes del control para ajustarse a una imagen.
-   Estire una imagen para ajustarla a los bordes del control.
-   Centrar una imagen dentro de los bordes del control.
-   Anclar una imagen en el área superior izquierda del control sin cambiar el tamaño de la imagen o el control (es posible que parte de la imagen no sea visible si no se cambia el tamaño de la imagen o el control).

## <a name="working-with-pictures-in-visual-studio-net"></a>Trabajar con imágenes en Visual Studio .NET

Para mostrar una imagen en tiempo de diseño en Visual Studio .NET:

1.  Arrastre un control [InkPicture](/previous-versions/aa514604(v=msdn.10)) en un formulario o haga doble clic en el control InkPicture en el cuadro de herramientas.
2.  En la ventana **propiedades** , seleccione la propiedad **imagen** y, a continuación, haga clic en el botón de puntos suspensivos para abrir el cuadro de diálogo **abrir** .
3.  Si busca un tipo de archivo específico (por ejemplo, archivos. jpg), selecciónelo en el cuadro **archivos de tipo** .
4.  Seleccione el archivo que desea mostrar.

Para borrar la imagen en tiempo de diseño:

1.  En la ventana **propiedades** , seleccione la propiedad **imagen** y haga clic con el botón secundario en la imagen en miniatura.
2.  Haga clic en **Restablecer**.

El control [InkPicture](/previous-versions/aa514604(v=msdn.10)) se muestra de forma predeterminada sin ningún borde. Puede proporcionar un borde estándar o tridimensional mediante la propiedad [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) para distinguir el cuadro InkPicture del resto del formulario, aunque no contenga ninguna imagen.

Puede mostrar una imagen en tiempo de ejecución con el método [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) del objeto [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



También puede incluir una imagen de fondo con la propiedad [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) del objeto de [imagen](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) heredado. sin embargo, no se puede cambiar el tamaño de esa imagen.

 

 
