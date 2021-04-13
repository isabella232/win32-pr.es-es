---
description: A partir de Windows 2000, los proveedores de servicios de telefonía que negocian una versión de 3,0 o posterior deben tener un proveedor de servicios multimedia correspondiente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicación del proveedor de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361894"
---
# <a name="media-service-provider-communication"></a>Comunicación del proveedor de servicios multimedia

A partir de Windows 2000, los proveedores de servicios de telefonía que negocian una versión de 3,0 o posterior deben tener un proveedor de servicios multimedia correspondiente. La división precisa de Responsabilidades operativas depende de la implementación. Por ejemplo, un TSP podría usar el MSP coincidente para realizar la determinación del tipo de medio en una sesión entrante. Sin embargo, el TSP debe cumplir el TSPI, lo que significa obtener esa determinación del MSP e informar a TAPI.

TSPI proporciona las siguientes funciones y mensajes para permitir una conexión virtual entre un TSP y un MSP:

-   [**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**LÍNEA \_ QOSINFO**](line-qosinfo.md)
-   [**LÍNEA \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
