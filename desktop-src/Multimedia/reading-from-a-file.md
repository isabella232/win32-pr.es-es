---
title: Leer de un archivo
description: Leer de un archivo
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076139"
---
# <a name="reading-from-a-file"></a>Leer de un archivo

Puede recuperar información sobre un archivo abierto mediante la función [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) . Esta función rellena la estructura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con información como la velocidad de datos máxima, el número de flujos del archivo, si el archivo usa un índice y si el archivo está protegido por derechos de autor.

Para recuperar información complementaria en un archivo AVI, utilice la función [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) . La información complementaria es aplicable a todo el archivo y no se incluye en los encabezados de archivo normales. Por ejemplo, el nombre de la empresa o la persona que contiene los derechos de autor de un archivo puede ser información complementaria. La información complementaria no se adhiere a un formato específico; puede ser específico del archivo. **AVIFileReadData** devuelve la información complementaria en un búfer proporcionado por la aplicación.

 

 




