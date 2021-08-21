---
title: Lectura desde un archivo
description: Lectura desde un archivo
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Función AVIFileInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95186b1ec8913623b0ab02e0d2bc5556302d4dcd03f7737ac12c5872b9f2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371710"
---
# <a name="reading-from-a-file"></a>Lectura desde un archivo

Puede recuperar información sobre un archivo abierto mediante la [**función AVIFileInfo.**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) Esta función rellena la estructura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con información como la velocidad de datos máxima, el número de secuencias del archivo, si el archivo usa un índice y si el archivo tiene derechos de propiedad intelectual.

Para recuperar información complementaria en un archivo AVI, use la [**función AVIFileReadData.**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) La información complementaria es aplicable a todo el archivo y no se incluye en los encabezados de archivo normales. Por ejemplo, el nombre de la empresa o la persona que contiene los derechos de autor de un archivo podría ser información complementaria. La información complementaria no se adhiere a un formato específico; puede ser específico del archivo. **AVIFileReadData** devuelve la información complementaria en un búfer proporcionado por la aplicación.

 

 




