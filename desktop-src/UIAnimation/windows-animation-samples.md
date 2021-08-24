---
title: Windows Ejemplos de animación
description: Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación Windows Animation Manager.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Windows Animation Windows Animation ,samples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9119ab7333f1f5d74b9be9998ad26b36139f9a92d88fec856d3f4572d12f431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656155"
---
# <a name="windows-animation-samples"></a>Windows Ejemplos de animación

Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación Windows Animation Manager.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Ejemplo de animación controlada por la aplicación](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Ejemplo de animación controlada por temporizador](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Ejemplo de interpolador personalizado](custom-interpolator-sample.md)<br/>                   | Muestra cómo usar Windows animación con su propio interpolador personalizado, con Direct2D usado para la representación. <br/> |
| [Ejemplo de diseño de cuadrícula](grid-layout-sample.md)<br/>                                   | Muestra cómo usar Windows animación mediante Direct2D para animar una cuadrícula de imágenes. <br/>                         |
| [Ejemplo de comparación de prioridad](priority-comparison-sample.md)<br/>                   | Muestra cómo usar la animación Windows con su propia comparación de prioridad, mediante Direct2D para la representación.<br/>      |



 

## <a name="sample-files"></a>Archivos de ejemplo

Cada ejemplo contiene muchos de los siguientes archivos de clave:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp
</dt> <dd>

Define el punto de entrada de la aplicación.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h
</dt> <dd>

Declara la clase CMainWindow.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp
</dt> <dd>

Inicializa los componentes de animación y la plataforma de gráficos, carga imágenes y representa el área de cliente.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h
</dt> <dd>

Declara la clase CLayoutManager.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp
</dt> <dd>

Calcula el diseño de las imágenes en la ventana principal, crea guiones gráficos, agrega transiciones al guión gráfico y programa el guión gráfico.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h
</dt> <dd>

Declara la clase CThumbNail.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp
</dt> <dd>

Crea variables de animación y representa miniaturas.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Guía de desarrollo de animaciones](windows-animation-developer-guide.md)
</dt> <dt>

[Windows Referencia de animación](windows-animation-reference.md)
</dt> </dl>

 

 





