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
# <a name="reading-from-compressed-files"></a><span data-ttu-id="31cd6-103">Leer archivos comprimidos</span><span class="sxs-lookup"><span data-stu-id="31cd6-103">Reading from Compressed Files</span></span>

<span data-ttu-id="31cd6-104">Además de descomprimir un archivo completo en una sola operación, una aplicación puede descomprimir un archivo comprimido en parte a la vez mediante las funciones [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) y [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) .</span><span class="sxs-lookup"><span data-stu-id="31cd6-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="31cd6-105">Estas funciones son especialmente útiles cuando es necesario extraer partes de archivos grandes.</span><span class="sxs-lookup"><span data-stu-id="31cd6-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="31cd6-106">Por ejemplo, un fabricante de fuentes puede tener archivos comprimidos que contengan métricas de fuentes además de datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="31cd6-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="31cd6-107">Para utilizar la información de estos archivos, una aplicación necesitaría descomprimir el archivo; sin embargo, la mayoría de las aplicaciones solo usarían parte del archivo en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="31cd6-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="31cd6-108">Para obtener información sobre las métricas de fuentes, la aplicación extraer datos del encabezado.</span><span class="sxs-lookup"><span data-stu-id="31cd6-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="31cd6-109">Para obtener información del texto, la aplicación volvería a colocar el puntero de archivo llamando a **LZSeek** y extraer los datos de caracteres llamando a **LZRead**.</span><span class="sxs-lookup"><span data-stu-id="31cd6-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



