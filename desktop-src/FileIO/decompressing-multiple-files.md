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
# <a name="decompressing-multiple-files"></a>Descomprimir varios archivos

Una aplicación puede descomprimir varios archivos realizando las siguientes tareas:

1.  Abra los archivos de código fuente mediante una llamada a la función [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Abra los archivos de destino mediante una llamada a [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copie los archivos de origen en los archivos de destino mediante una llamada a la función [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .
4.  Cierre los archivos mediante una llamada a la función [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



