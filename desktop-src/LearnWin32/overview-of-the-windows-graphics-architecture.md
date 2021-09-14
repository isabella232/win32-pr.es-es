---
title: Introducción a la arquitectura Windows gráficos
description: Describe las API de gráficos de C++/COM en Windows.
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159946"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Introducción a la arquitectura Windows gráficos

Windows proporciona varias API de C++/COM para gráficos. Estas API se muestran en el diagrama siguiente.

![diagrama que muestra las API de gráficos de Windows.](images/graphics01.png)

-   Interfaz de dispositivo gráfico (GDI) es la interfaz gráfica original para Windows. GDI se escribió primero para archivos de 16 Windows y, a continuación, se actualizó para archivos de 32 y 64 Windows.
-   GDI+ se introdujo en Windows XP como sucesor de GDI. Se GDI+ acceso a la biblioteca a través de un conjunto de clases de C++ que encapsulan funciones de C planas. El .NET Framework también proporciona una versión administrada de GDI+ en el espacio **de nombres System.Drawing.**
-   Direct3D admite gráficos 3D.
-   Direct2D es una API moderna para gráficos 2D, la sucesora de GDI y GDI+.
-   DirectWrite es un motor de rasterización y diseño de texto. Puede usar GDI o Direct2D para dibujar el texto rasterizado.
-   Infraestructura de gráficos de DirectX (DXGI) realiza tareas de bajo nivel, como presentar fotogramas para la salida. La mayoría de las aplicaciones no usan DXGI directamente. En su lugar, actúa como una capa intermedia entre el controlador de gráficos y Direct3D.

Direct2D y DirectWrite se introdujeron en Windows 7. También están disponibles para Windows Vista y Windows Server 2008 a través de una actualización de plataforma. Para obtener más información, vea [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

Direct2D es el foco de este módulo. Aunque GDI y GDI+ siguen siendo compatibles en Windows, se recomiendan Direct2D y DirectWrite para los nuevos programas. En algunos casos, una combinación de tecnologías podría ser más práctica. En estas situaciones, Direct2D y DirectWrite están diseñados para interoperar con GDI.

En las secciones siguientes se describen algunas de las ventajas de Direct2D.

### <a name="hardware-acceleration"></a>Aceleración de hardware

El término *aceleración de hardware* hace referencia a los cálculos gráficos realizados por la unidad de procesamiento gráfico (GPU), en lugar de la CPU. Las GPU modernas están muy optimizadas para los tipos de cálculo que se usan en la representación de gráficos. Por lo general, cuando más trabajo se mueve de la CPU a la GPU, mejor.

Aunque GDI admite la aceleración de hardware para ciertas operaciones, muchas operaciones GDI están enlazadas a la CPU. Direct2D está en capas sobre Direct3D y aprovecha al máximo la aceleración de hardware proporcionada por la GPU. Si la GPU no admite las características necesarias para Direct2D, Direct2D vuelve a la representación de software. En general, Direct2D supera a GDI y GDI+ en la mayoría de las situaciones.

### <a name="transparency-and-anti-aliasing"></a>Transparencia y suavizado de alias

Direct2D admite la combinación alfa acelerada por hardware (transparencia).

GDI tiene compatibilidad limitada con la mezcla alfa. La mayoría de las funciones de GDI no admiten la combinación alfa, aunque GDI admite la mezcla alfa durante una operación de bit a bit. GDI+ admite la transparencia, pero la mezcla alfa la realiza la CPU, por lo que no se beneficia de la aceleración de hardware.

La combinación alfa acelerada por hardware también habilita el suavizado de alias. *El alias* es un artefacto causado por el muestreo de una función continua. Por ejemplo, cuando una línea curva se convierte en píxeles, el alias puede provocar una apariencia irregular. \[ 3 Cualquier técnica que reduzca los artefactos causados por el alias se \] considera una forma de suavizado de alias. En gráficos, el suavizado de contorno se realiza combinando los bordes con el fondo. Por ejemplo, este es un círculo dibujado por GDI y el mismo círculo dibujado por Direct2D.

![ilustración de técnicas de suavizado de alias en direct2d.](images/graphics02.png)

En la imagen siguiente se muestra un detalle de cada círculo.

![un detalle de la imagen anterior.](images/graphics03.png)

El círculo dibujado por GDI (izquierda) consta de píxeles negros que se aproximan a una curva. El círculo dibujado por Direct2D (derecha) usa la combinación para crear una curva más suave.

GDI no admite suavizado de contorno cuando dibuja geometría (líneas y curvas). GDI puede dibujar texto con suavizado de alias mediante ClearType; pero, de lo contrario, el texto GDI también tiene alias. El alias es especialmente perceptible para el texto, porque las líneas irregulares interrumpen el diseño de fuentes, lo que hace que el texto sea menos legible. Aunque GDI+ admite el suavizado de alias, lo aplica la CPU, por lo que el rendimiento no es tan bueno como Direct2D.

### <a name="vector-graphics"></a>Gráficos vectoriales

Direct2D admite *gráficos vectoriales.* En gráficos vectoriales, las fórmulas matemáticas se usan para representar líneas y curvas. Estas fórmulas no dependen de la resolución de pantalla, por lo que se pueden escalar a dimensiones arbitrarias. Los gráficos vectoriales son especialmente útiles cuando se debe escalar una imagen para admitir diferentes tamaños de monitor o resoluciones de pantalla.

## <a name="next"></a>Siguientes

[El Administrador de ventanas de escritorio](the-desktop-window-manager.md)

 

 
