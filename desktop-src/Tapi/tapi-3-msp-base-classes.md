---
description: En este documento se describe el diseño y el uso de las clases base de MSP. El uso de estas clases no es necesario, pero la mayoría de los desarrolladores encontrarán que simplifican la tarea de crear un MSP basado en DirectShow para TAPI 3S New MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Clases base de TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678358"
---
# <a name="tapi-3-msp-base-classes"></a>Clases base de TAPI 3 MSP

En este documento se describe el diseño y el uso de las clases base de MSP. El uso de estas clases no es necesario, pero la mayoría de los desarrolladores encontrarán que simplifican la tarea de compilar un MSP nuevo basado en DirectShow para MSPI nuevos de TAPI 3.

El código fuente de las clases base MSP se puede encontrar en el directorio Samples del kit de desarrollo de software (SDK) de la plataforma.

Se supone que está familiarizado con COM, ATL, DirectShow y C++. El lector también debe conocer el material general de [acerca del proveedor de servicios multimedia (MSP)](about-the-media-service-provider-msp-.md) y de la [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-.md).

ATL 2,1 es necesario para Windows 2000. A partir de Windows XP, se compilarán tanto ATL 2,1 como 3,0.

Bibliotecas de clases base MSP (disponibles en el SDK):

-   Mspbase. lib
-   Mspid. lib
-   Strmbase. lib
-   Tmuid. lib
    > [!Note]  
    > Se debe usar la vinculación dinámica en lugar de estática.

     

Archivos de encabezado de clase base MSP (disponibles en el SDK):

-   Mspaddr. h
-   Mspbase. h
-   Mspcall. h
-   Msplog. h
-   Mspstrm. h
-   Mspterm. h
-   Mspthrd. h
-   Msptmac. h
-   Msptmvc. h
-   Msptrmvc. h
-   Msptrmac. h
-   Msptrmar. h
-   Msputils. h

Archivos de origen de la clase base MSP (disponibles en los ejemplos del SDK):

-   Mspaddr. cpp
-   Mspcall. cpp
-   Msplog. cpp
-   Mspstrm. cpp
-   Mspterm. cpp
-   Mspthrd. cpp
-   Msptrmac. cpp
-   Msptrmar. cpp
-   Msptrmvc. cpp
-   Msputils. cpp

 

 



