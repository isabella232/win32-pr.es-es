---
description: En este documento se describe el diseño y el uso de las clases base de MSP. El uso de estas clases no es necesario, pero la mayoría de los desarrolladores encontrarán que simplifican la tarea de crear un MSP basado en DirectShow para el nuevo MSPI de TAPI 3s.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Clases base de MSP de TAPI 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34d4f9f67618c3637bfaff149773ab7b0de4b93f33c8bca8e5eb892527735e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012345"
---
# <a name="tapi-3-msp-base-classes"></a>Clases base de MSP de TAPI 3

En este documento se describe el diseño y el uso de las clases base de MSP. No es necesario usar estas clases, pero la mayoría de los desarrolladores encontrarán que simplifican la tarea de crear un MSP basado en DirectShow para el nuevo MSPI de TAPI 3.

El código fuente de las clases base de MSP se puede encontrar en el directorio Ejemplos del Kit de desarrollo de software (SDK) de plataforma.

Se supone que está familiarizado con COM, ATL, DirectShow y C++. El lector también debe conocer el material general en Acerca del proveedor de [Media Service (MSP)](about-the-media-service-provider-msp-.md) y en La interfaz del proveedor de servicios multimedia [(MSPI).](media-service-provider-interface-mspi-.md)

Atl 2.1 es necesario para Windows 2000. A partir Windows XP, atl 2.1 y 3.0 se compilarán.

Bibliotecas de clases base de MSP (disponibles en el SDK):

-   Mspbase.lib
-   Mspid.lib
-   Strmbase.lib
-   Tmuid.lib
    > [!Note]  
    > Se debe usar la vinculación dinámica en lugar de estática.

     

Archivos de encabezado de clase base de MSP (disponibles en el SDK):

-   Mspaddr.h
-   Mspbase.h
-   Mspcall.h
-   Msplog.h
-   Mspstrm.h
-   Mspterm.h
-   Mspthrd.h
-   Msptmac.h
-   Msptmvc.h
-   Msptrmvc.h
-   Msptrmac.h
-   Msptrmar.h
-   Msputils.h

Archivos de origen de clase base de MSP (disponibles en los ejemplos del SDK):

-   Mspaddr.cpp
-   Mspcall.cpp
-   Msplog.cpp
-   Mspstrm.cpp
-   Mspterm.cpp
-   Mspthrd.cpp
-   Msptrmac.cpp
-   Msptrmar.cpp
-   Msptrmvc.cpp
-   Msputils.cpp

 

 



