---
description: Una aplicación puede descomprimir un solo archivo comprimido mediante las funciones LZOpenFile, LZCopy y LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Descompresión de un solo archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687284"
---
# <a name="decompressing-a-single-file"></a><span data-ttu-id="e8290-103">Descompresión de un solo archivo</span><span class="sxs-lookup"><span data-stu-id="e8290-103">Decompressing a Single File</span></span>

<span data-ttu-id="e8290-104">Una aplicación puede descomprimir un solo archivo comprimido realizando las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="e8290-104">An application can decompress a single compressed file by performing the following tasks:</span></span>

1.  <span data-ttu-id="e8290-105">Abra el archivo de código fuente mediante una llamada a la función [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="e8290-105">Open the source file by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="e8290-106">Abra el archivo de destino mediante una llamada a [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="e8290-106">Open the destination file by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="e8290-107">Copie el archivo de origen en el archivo de destino mediante una llamada a la función [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) y pasando los identificadores devueltos por [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="e8290-107">Copy the source file to the destination file by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function and passing the handles returned by [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
4.  <span data-ttu-id="e8290-108">Cierre los archivos mediante una llamada a la función [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="e8290-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



