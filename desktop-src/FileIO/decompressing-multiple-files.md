---
description: Una aplicación puede descomprimir varios archivos mediante las funciones LZOpenFile, LZCopy y LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Descomprimir varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687281"
---
# <a name="decompressing-multiple-files"></a><span data-ttu-id="e949f-103">Descomprimir varios archivos</span><span class="sxs-lookup"><span data-stu-id="e949f-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="e949f-104">Una aplicación puede descomprimir varios archivos realizando las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="e949f-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="e949f-105">Abra los archivos de código fuente mediante una llamada a la función [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="e949f-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="e949f-106">Abra los archivos de destino mediante una llamada a [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="e949f-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="e949f-107">Copie los archivos de origen en los archivos de destino mediante una llamada a la función [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .</span><span class="sxs-lookup"><span data-stu-id="e949f-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="e949f-108">Cierre los archivos mediante una llamada a la función [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="e949f-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



