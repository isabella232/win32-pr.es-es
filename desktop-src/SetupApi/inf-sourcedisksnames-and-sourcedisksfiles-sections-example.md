---
description: La sección SourceDisksNames de un archivo INF identifica los discos que contienen los archivos de origen que se están instalando.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667996"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF

La sección **SourceDisksNames** de un archivo INF identifica los discos que contienen los archivos de origen que se están instalando. La sección **SourceDisksFiles** identifica los archivos de origen y los discos de origen que los contienen. Tenga en cuenta que las plataformas MIPS, Alpha y PPC no son compatibles con Windows 2000 o Windows XP.

A partir de Windows XP, una sección **SourceDisksNames** puede especificar una etiqueta y un archivo. cab. Por ejemplo, la siguiente sección **SourceDisksNames** se puede usar con medios extraíbles o fijos. Si se usa un medio extraíble, en la sección de ejemplo se comprueba la presencia del medio comprobando en primer lugar la presencia de la etiqueta. Si usa medios fijos, en la sección de ejemplo se comprueba la presencia del medio comprobando primero la presencia del archivo. cab. Después de comprobar la presencia de un archivo. cab, el sistema intenta copiar archivos fuera del archivo. cab y solicita los archivos que no se pudieron copiar.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Para obtener más información acerca de **SourceDisksNames** o **SourceDisksFiles**, vea las secciones "instrucciones generales para el archivo INF" y "secciones y directivas de archivos INF" del kit de desarrollo de controladores de Microsoft Windows 2000.

 

 



