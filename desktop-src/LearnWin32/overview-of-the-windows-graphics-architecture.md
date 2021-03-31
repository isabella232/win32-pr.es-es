---
title: Información general de la arquitectura de gráficos de Windows
description: Describe las API de gráficos de C++/COM en Windows.
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "104156976"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Información general de la arquitectura de gráficos de Windows

Windows proporciona varias API/COM de C++ para gráficos. Estas API se muestran en el diagrama siguiente.

![diagrama que muestra las API de gráficos de Windows.](images/graphics01.png)

-   Interfaz de dispositivo gráfico (GDI) es la interfaz de gráficos original para Windows. GDI se escribió por primera vez para Windows de 16 bits y, a continuación, se actualizó en Windows de 32 y 64 bits.
-   GDI+ se incorporó en Windows XP como sucesor de GDI. Se tiene acceso a la biblioteca GDI+ a través de un conjunto de clases de C++ que ajustan las funciones planas de C. El .NET Framework también proporciona una versión administrada de GDI+ en el espacio de nombres **System. Drawing** .
-   Direct3D admite gráficos 3D.
-   Direct2D es una API moderna para gráficos 2D, el sucesor de GDI y GDI+.
-   DirectWrite es un motor de diseño y rasterización de texto. Puede usar GDI o Direct2D para dibujar el texto rasterizado.
-   La infraestructura de gráficos de DirectX (DXGI) realiza tareas de bajo nivel, como presentar fotogramas para la salida. La mayoría de las aplicaciones no usan DXGI directamente. En su lugar, sirve como capa intermedia entre el controlador de gráficos y Direct3D.

Direct2D y DirectWrite se introdujeron en Windows 7. También están disponibles para Windows Vista y Windows Server 2008 a través de una actualización de la plataforma. Para obtener más información, consulte [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

Direct2D es el centro de este módulo. Aunque tanto GDI como GDI+ siguen siendo compatibles con Windows, se recomiendan Direct2D y DirectWrite para los nuevos programas. En algunos casos, es posible que una combinación de tecnologías sea más práctica. En estas situaciones, Direct2D y DirectWrite están diseñados para interoperar con GDI.

En las secciones siguientes se describen algunas de las ventajas de Direct2D.

### <a name="hardware-acceleration"></a>Aceleración de hardware

El término *aceleración de hardware* hace referencia a los cálculos de gráficos realizados por la unidad de procesamiento de gráficos (GPU), en lugar de la CPU. Las GPU modernas están muy optimizadas para los tipos de cálculo que se usan en la representación de gráficos. Por lo general, cuanto mayor sea el trabajo que se mueva de la CPU a la GPU, mejor.

Aunque GDI admite la aceleración de hardware para ciertas operaciones, muchas operaciones de GDI están enlazadas a la CPU. Direct2D está superpuesto a Direct3D y saca el máximo partido de la aceleración de hardware proporcionada por la GPU. Si la GPU no es compatible con las características necesarias para Direct2D, Direct2D recurre a la representación de software. En general, Direct2D supera GDI y GDI+ en la mayoría de los casos.

### <a name="transparency-and-anti-aliasing"></a>Transparencia y suavizado de contorno

Direct2D admite la combinación alfa (transparencia) totalmente acelerada por hardware.

GDI tiene compatibilidad limitada con la combinación alfa. La mayoría de las funciones GDI no admiten la combinación alfa, aunque GDI admite la combinación alfa durante una operación BitBlt. GDI+ admite la transparencia, pero la combinación alfa la realiza la CPU, por lo que no se beneficia de la aceleración de hardware.

La combinación alfa acelerada por hardware también habilita el suavizado de contorno. El *alias* es un artefacto causado por el muestreo de una función continua. Por ejemplo, cuando una línea curva se convierte en píxeles, el alias puede producir una apariencia escalonada. \[ 3 \] cualquier técnica que reduzca los artefactos causados por el alias se considera una forma de suavizado de contorno. En los gráficos, el suavizado de contorno se realiza combinando los bordes con el fondo. Por ejemplo, a continuación se muestra un círculo dibujado por GDI y el mismo círculo dibujado por Direct2D.

![Ilustración de técnicas de suavizado de contorno en direct2d.](images/graphics02.png)

La siguiente imagen muestra un detalle de cada círculo.

![detalle de la imagen anterior.](images/graphics03.png)

El círculo dibujado por GDI (izquierda) se compone de píxeles negros que se aproximan a una curva. El círculo dibujado por Direct2D (right) usa la combinación para crear una curva más suave.

GDI no admite el suavizado de contorno cuando dibuja geometría (líneas y curvas). GDI puede dibujar texto suavizado mediante ClearType; pero en caso contrario, el texto GDI también tiene alias. El alias es especialmente evidente para el texto, porque las líneas irregulares interrumpen el diseño de la fuente, lo que permite que el texto sea menos legible. Aunque GDI+ admite el suavizado de contorno, se aplica mediante la CPU, por lo que el rendimiento no es tan bueno como Direct2D.

### <a name="vector-graphics"></a>Gráficos vectoriales

Direct2D admite *gráficos vectoriales*. En los gráficos vectoriales, las fórmulas matemáticas se utilizan para representar líneas y curvas. Estas fórmulas no dependen de la resolución de pantalla, por lo que se pueden escalar a dimensiones arbitrarias. Los gráficos vectoriales son especialmente útiles cuando una imagen se debe escalar para admitir diferentes tamaños de monitor o resoluciones de pantalla.

## <a name="next"></a>Siguientes

[El Administrador de ventanas de escritorio](the-desktop-window-manager.md)

 

 
