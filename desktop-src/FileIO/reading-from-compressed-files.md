---
description: Una aplicación puede descomprimir un archivo comprimido una parte a la vez mediante las funciones LZSeek y LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lectura desde archivos comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069862"
---
# <a name="reading-from-compressed-files"></a>Lectura desde archivos comprimidos

Además de descomprimir un archivo completo en una sola operación, una aplicación puede descomprimir un archivo comprimido una parte a la vez mediante las funciones [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) y [**LZRead.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) Estas funciones son especialmente útiles cuando es necesario extraer partes de archivos grandes. Por ejemplo, un fabricante de fuentes puede tener archivos comprimidos que contienen métricas de fuente además de datos de caracteres. Para usar la información de estos archivos, una aplicación tendría que descomprimir el archivo; sin embargo, la mayoría de las aplicaciones usarían solo una parte del archivo en un momento determinado. Para obtener información sobre las métricas de fuente, la aplicación extraería datos del encabezado . Para obtener información del texto, la aplicación cambiaría la posición del puntero de archivo llamando a **LZSeek** y extrayendo datos de caracteres llamando **a LZRead**.

 

 



