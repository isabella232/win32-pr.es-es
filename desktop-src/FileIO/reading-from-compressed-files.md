---
description: Una aplicación puede descomprimir un archivo comprimido una parte a la vez mediante las funciones LZSeek y LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lectura desde archivos comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5ccc99aa20fc36f1055f22c01fbd4cab25337badeabbf34b02023889b7f3d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914505"
---
# <a name="reading-from-compressed-files"></a>Lectura desde archivos comprimidos

Además de descomprimir un archivo completo en una sola operación, una aplicación puede descomprimir un archivo comprimido una parte a la vez mediante las funciones [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) y [**LZRead.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) Estas funciones son especialmente útiles cuando es necesario extraer partes de archivos grandes. Por ejemplo, un fabricante de fuentes puede tener archivos comprimidos que contienen métricas de fuente además de datos de caracteres. Para usar la información de estos archivos, una aplicación tendría que descomprimir el archivo; sin embargo, la mayoría de las aplicaciones usarían solo una parte del archivo en un momento determinado. Para obtener información sobre las métricas de fuente, la aplicación extraería datos del encabezado . Para obtener información del texto, la aplicación cambiaría la posición del puntero de archivo llamando a **LZSeek** y extrayendo datos de caracteres mediante una llamada **a LZRead**.

 

 



