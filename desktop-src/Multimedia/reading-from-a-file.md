---
title: Lectura desde un archivo
description: Lectura desde un archivo
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Función AVIFileInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372014"
---
# <a name="reading-from-a-file"></a>Lectura desde un archivo

Puede recuperar información sobre un archivo abierto mediante la [**función AVIFileInfo.**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) Esta función rellena la estructura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con información como la velocidad de datos máxima, el número de secuencias del archivo, si el archivo usa un índice y si el archivo tiene derechos de autor.

Para recuperar información complementaria en un archivo AVI, use la [**función AVIFileReadData.**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) La información adicional es aplicable a todo el archivo y no se incluye en los encabezados de archivo normales. Por ejemplo, el nombre de la empresa o la persona que contiene los derechos de propiedad intelectual de un archivo podría ser información adicional. La información complementaria no se adhiere a un formato específico; puede ser específico del archivo. **AVIFileReadData** devuelve la información complementaria en un búfer proporcionado por la aplicación.

 

 




