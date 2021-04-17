---
description: Una aplicación puede descomprimir un archivo comprimido en parte a la vez mediante las funciones LZSeek y LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Leer archivos comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688124"
---
# <a name="reading-from-compressed-files"></a>Leer archivos comprimidos

Además de descomprimir un archivo completo en una sola operación, una aplicación puede descomprimir un archivo comprimido en parte a la vez mediante las funciones [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) y [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) . Estas funciones son especialmente útiles cuando es necesario extraer partes de archivos grandes. Por ejemplo, un fabricante de fuentes puede tener archivos comprimidos que contengan métricas de fuentes además de datos de caracteres. Para utilizar la información de estos archivos, una aplicación necesitaría descomprimir el archivo; sin embargo, la mayoría de las aplicaciones solo usarían parte del archivo en un momento determinado. Para obtener información sobre las métricas de fuentes, la aplicación extraer datos del encabezado. Para obtener información del texto, la aplicación volvería a colocar el puntero de archivo llamando a **LZSeek** y extraer los datos de caracteres llamando a **LZRead**.

 

 



