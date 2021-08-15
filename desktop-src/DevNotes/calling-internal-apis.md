---
description: El archivo de encabezado Denl.h expone prototipos de API Windows internas. No hay ninguna biblioteca de importación asociada, por lo que los desarrolladores deben usar la vinculación dinámica en tiempo de ejecución para llamar a las funciones descritas en este archivo de encabezado.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Llamar a las API internas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c613b4f650709eb9764eff133c018be62768c58212b4dc7130149ce8b5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956134"
---
# <a name="calling-internal-apis"></a>Llamar a las API internas

El archivo de encabezado Denl.h expone prototipos de API Windows internas. No hay ninguna biblioteca de importación asociada, por lo que los desarrolladores deben usar la vinculación dinámica en tiempo de ejecución para llamar a las funciones descritas en este archivo de encabezado.

Las funciones y estructuras de Winternl.h son internas del sistema operativo y están sujetas a cambios de una versión de Windows a la siguiente, y posiblemente incluso entre Service Pack para cada versión. Para mantener la compatibilidad de la aplicación, debe usar las funciones públicas equivalentes en su lugar. Hay más información disponible en el archivo de encabezado, Invernal.h, y la documentación de cada función.

Si usa estas funciones, puede acceder a ellas mediante la vinculación dinámica en tiempo de ejecución mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Esto ofrece al código la oportunidad de responder correctamente si la función se ha cambiado o quitado del sistema operativo. Sin embargo, es posible que los cambios de firma no sean detectables.

 

 
