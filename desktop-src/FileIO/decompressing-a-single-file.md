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
# <a name="decompressing-a-single-file"></a>Descompresión de un solo archivo

Una aplicación puede descomprimir un solo archivo comprimido realizando las siguientes tareas:

1.  Abra el archivo de código fuente mediante una llamada a la función [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Abra el archivo de destino mediante una llamada a [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copie el archivo de origen en el archivo de destino mediante una llamada a la función [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) y pasando los identificadores devueltos por [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Cierre los archivos mediante una llamada a la función [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



