---
description: La sección SourceDisksNames de un archivo INF identifica los discos que contienen los archivos de origen que se están instalando.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00eb8241b8e290f5460cc41b233d3b199df35e709d6e32f2c5a39925a79f851d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739415"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF

La **sección SourceDisksNames** de un archivo INF identifica los discos que contienen los archivos de origen que se están instalando. La **sección SourceDisksFiles** identifica los archivos de origen y los discos de origen que los contienen. Tenga en cuenta que las plataformas MIPS, Alpha y PPC no son compatibles con Windows 2000 o Windows XP.

A partir Windows XP, una **sección SourceDisksNames** puede especificar una etiqueta y un archivo de archivado. Por ejemplo, la siguiente **sección SourceDisksNames** se puede usar con medios extraíbles o fijos. Si usa medios extraíbles, la sección de ejemplo comprueba la presencia del medio comprobando primero la presencia de la etiqueta . Si usa medios fijos, la sección de ejemplo comprueba la presencia de los medios comprobando primero la presencia del gabinete. Después de comprobar la presencia de un gabinete, el sistema intenta copiar archivos fuera del gabinete y solicita los archivos que no pudo copiar.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Para obtener más información sobre **SourceDisksNames** o **SourceDisksFiles**, vea las secciones "Instrucciones generales para el archivo INF" y "Secciones y directivas de archivo INF" del Kit de desarrollo de controladores de Microsoft Windows 2000.

 

 



