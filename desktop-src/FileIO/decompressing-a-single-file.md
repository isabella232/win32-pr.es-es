---
description: Una aplicación puede descomprimir un único archivo comprimido mediante las funciones LZOpenFile, LZCopy y LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Descomprimir un solo archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99152a36a2846bfe35a9d92bc3d8fd2eb6b5c3a7f0877179262801a9141bcc61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150841"
---
# <a name="decompressing-a-single-file"></a>Descomprimir un solo archivo

Una aplicación puede descomprimir un único archivo comprimido realizando las siguientes tareas:

1.  Abra el archivo de código fuente mediante una llamada a [**la función LZOpenFile.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)
2.  Abra el archivo de destino mediante una llamada [**a LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copie el archivo de origen en el archivo de destino llamando a la función [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) y pasando los identificadores devueltos [**por LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Cierre los archivos mediante una llamada a la [**función LZClose.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose)

 

 



