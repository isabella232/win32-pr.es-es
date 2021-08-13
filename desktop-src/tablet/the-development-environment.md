---
description: No necesita una tableta pc para desarrollar aplicaciones de Tablet PC, pero necesita un equipo personal capaz de ejecutar el software que aparece más adelante en este tema.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: El entorno de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d6c0de35fa84ec4ee01b3f25aaefec6ab3470fde83161f7aaf2157197bbf1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449218"
---
# <a name="the-development-environment"></a>El entorno de desarrollo

No necesita una tableta pc para desarrollar aplicaciones de Tablet PC, pero necesita un equipo personal capaz de ejecutar el software que aparece más adelante en este tema.

Se recomienda encarecidamente probar la aplicación en un tablet PC real para asegurarse de que se tienen en cuenta todas las diferencias en el hardware, como el digitalizador de mayor resolución.

Un sistema de desarrollo típico y mínimo consta del siguiente hardware y software.

## <a name="hardware"></a>Hardware

-   8 MB de espacio en disco duro para una instalación completa.
-   Un dispositivo que apunta para la entrada. Esto incluye dispositivos como un mouse, una tableta externa o un tablet PC con un digitalizador HID.

HID significa Dispositivo de interfaz humana, un estándar para dispositivos de entrada. Los digitalizadores no compatibles con HID se tratan como un mouse normal, mientras que los digitalizadores compatibles con HID tienen una mayor resolución y más metadatos en trazos, como presión, similares a los instalados en el hardware de tablet PC.

## <a name="software"></a>Software

Los siguientes sistemas operativos se pueden usar para desarrollar aplicaciones de Tablet PC:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

También necesita lo siguiente:

-   Visual Studio versión 6 con Service Pack 5 o Visual Studio .NET o Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 o superior (recomendado)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Detalles sobre el desarrollo en SKU de PC que no son tabletas de Windows

Los componentes de la plataforma tablet PC se pueden instalar en Windows XP Professional con Service Pack 2 o Windows Server 2003. En estos sistemas operativos, la aplicación puede recopilar entrada de lápiz con la clase [**InkCollector**](inkcollector-class.md) y se puede probar y depurar. Sin embargo, no hay ningún reconocimiento disponible a menos que también instale Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack. Puede descargar ese paquete desde el Centro de descarga en MSDN.

Después de instalar el SDK de Windows en un sistema de Windows XP Professional o Windows Server 2003, tendrá todos los archivos de desarrollo necesarios para compilar aplicaciones de entrada de lápiz (como msbizut.h para un desarrollador COM). Sin embargo, no podrá ejecutar ni depurar la aplicación en ese sistema hasta que instale los archivos en tiempo de ejecución. Por ejemplo, en el caso de un desarrollador COM, inkobj.dll debe instalarse y registrarse. Dado que no está en un sistema donde existen estos archivos de plataforma, debe instalar los componentes de la plataforma de Tablet PC desde el módulo de combinación redistribuible, mstpcrt.msm, para obtener los archivos en tiempo de ejecución en el sistema.

La manera más sencilla de instalar los entornos de ejecución de la plataforma en un sistema Windows XP Professional o Windows 2000 con fines de desarrollo es compilar el proyecto de instalación de ejemplo proporcionado con los ejemplos de PC móvil y tablet PC e implementarlo en la máquina de desarrollo.

> [!Note]  
> Windows Vista y Windows XP Tablet PC Edition 2005 ya tienen instalados los componentes de la plataforma, por lo que no requieren pasos adicionales para ejecutar y depurar aplicaciones de Tablet PC.

 

Los controles [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) se pueden usar para recopilar entradas de lápiz en Windows 2000 con Service Pack 4 o Windows XP Professional con Service Pack 2 cuando los componentes de la plataforma de Tablet PC están presentes mediante la instalación de la versión 1.7 del SDK de Tablet PC, pero no pueden recopilar la entrada de lápiz en sistemas que no son de tableta que no tienen instalados los componentes de la plataforma tablet PC.

El SDK Windows proporciona todos los componentes necesarios para desarrollar aplicaciones de Tablet PC en SKU que no son de tableta de Windows. Establezca la siguiente clave del Registro **DWORD** en 1 para recopilar entradas de lápiz en SKU que no son de tableta de Windows:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Esta clave está pensada solo para fines de desarrollo.

 

 



