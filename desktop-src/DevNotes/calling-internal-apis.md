---
description: El archivo de encabezado Winternl. h expone prototipos de API de Windows internas. No hay ninguna biblioteca de importación asociada, por lo que los desarrolladores deben usar la vinculación dinámica en tiempo de ejecución para llamar a las funciones descritas en este archivo de encabezado.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Llamar a API internas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998254"
---
# <a name="calling-internal-apis"></a>Llamar a API internas

El archivo de encabezado Winternl. h expone prototipos de API de Windows internas. No hay ninguna biblioteca de importación asociada, por lo que los desarrolladores deben usar la vinculación dinámica en tiempo de ejecución para llamar a las funciones descritas en este archivo de encabezado.

Las funciones y estructuras de Winternl. h son internas del sistema operativo y están sujetas a cambios de una versión de Windows a la siguiente y, posiblemente, incluso entre los Service Pack de cada versión. Para mantener la compatibilidad de la aplicación, debe usar en su lugar las funciones públicas equivalentes. Hay más información disponible en el archivo de encabezado, Winternl. h, y en la documentación de cada función.

Si usa estas funciones, puede tener acceso a ellas a través de la vinculación dinámica en tiempo de ejecución mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Esto proporciona al código una oportunidad para responder correctamente si la función se ha cambiado o quitado del sistema operativo. Sin embargo, es posible que los cambios en la firma no se puedan detectar.

 

 
