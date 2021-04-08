---
description: No necesita un Tablet PC para desarrollar aplicaciones de Tablet PC, pero sí necesita un equipo personal capaz de ejecutar el software que se muestra más adelante en este tema.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: El entorno de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003067"
---
# <a name="the-development-environment"></a>El entorno de desarrollo

No necesita un Tablet PC para desarrollar aplicaciones de Tablet PC, pero sí necesita un equipo personal capaz de ejecutar el software que se muestra más adelante en este tema.

Se recomienda encarecidamente que pruebe la aplicación en un Tablet PC real para asegurarse de que se tienen en cuenta todas las diferencias en el hardware, como el digitalizador de mayor resolución.

Un sistema de desarrollo típico y mínimo consta del siguiente hardware y software.

## <a name="hardware"></a>Hardware

-   8 MB de espacio en disco duro para una instalación completa.
-   Un dispositivo señalador para la entrada. Esto incluye dispositivos como un mouse, una tableta externa o un Tablet PC con un digitalizador HID.

HID significa Dispositivo de interfaz humana, un estándar para dispositivos de entrada. Los digitalizadores que no son compatibles con HID se tratan como un mouse normal, mientras que los digitalizadores compatibles con HID tienen una mayor resolución y más metadatos en los trazos, como la presión, similar a los que están instalados en el hardware de Tablet PC.

## <a name="software"></a>Software

Los siguientes sistemas operativos se pueden usar para desarrollar aplicaciones de Tablet PC:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

También necesita lo siguiente:

-   Visual Studio versión 6 con Service Pack 5, Visual Studio .NET o Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 o posterior (recomendado)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Detalles sobre el desarrollo en SKU que no son de Tablet PC de Windows

Los componentes de la plataforma de Tablet PC se pueden instalar en Windows XP Professional con Service Pack 2 o Windows Server 2003. En estos sistemas operativos, la aplicación puede recopilar entradas manuscritas con la clase [**InkCollector**](inkcollector-class.md) y se puede probar y depurar. Sin embargo, no hay ningún reconocimiento disponible a menos que también Instale el paquete de reconocimiento de Microsoft Windows XP Tablet PC Edition 2005. Puede descargar ese paquete desde el centro de descarga de en MSDN.

Después de instalar el Windows SDK en un sistema Windows XP Professional o Windows Server 2003, tendrá todos los archivos de desarrollo necesarios para compilar aplicaciones de entrada manuscrita (como msinkaut. h para un desarrollador COM). Sin embargo, no podrá ejecutar ni depurar la aplicación en ese sistema hasta que instale los archivos en tiempo de ejecución. Por ejemplo, en el caso de un desarrollador COM, inkobj.dll se debe instalar y registrar. Dado que no está en un sistema donde existan estos archivos de plataforma, debe instalar los componentes de la plataforma de Tablet PC del módulo de combinación redistribuible, mstpcrt. MSM, para obtener los archivos en tiempo de ejecución en el sistema.

La manera más sencilla de obtener los tiempos de ejecución de la plataforma instalados en un sistema Windows XP Professional o Windows 2000 con fines de desarrollo consiste en compilar el proyecto de instalación de ejemplo que se proporciona con los ejemplos de PC móvil y Tablet PC e implementarlo en el equipo de desarrollo.

> [!Note]  
> Windows Vista y Windows XP Tablet PC Edition 2005 ya tienen instalados los componentes de la plataforma, por lo que no requieren pasos adicionales para ejecutar y depurar aplicaciones de Tablet PC.

 

Los controles [InkEdit](inkedit-control-reference.md) y [InkPicture](inkpicture-control-reference.md) se pueden usar para recopilar la entrada de lápiz en Windows 2000 con Service Pack 4 o Windows XP Professional con Service Pack 2 cuando los componentes de la plataforma de Tablet PC están presentes instalando la versión 1,7 del SDK de Tablet PC, pero no pueden recopilar entradas de lápiz en sistemas que no son de Tablet PC y que no tienen instalados los componentes de la plataforma de Tablet

La Windows SDK proporciona todos los componentes necesarios para desarrollar aplicaciones de Tablet PC en SKU que no son de Tablet PC de Windows. Establezca la siguiente clave **DWORD** del registro en 1 para recopilar la entrada de lápiz en las SKU de Windows que no son de Tablet PC:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Esta clave está pensada solo para fines de desarrollo.

 

 



