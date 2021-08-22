---
description: A partir Windows proveedores de servicios de telefonía 2000 que negocien una versión de 3.0 o posterior deben tener un proveedor de servicios multimedia correspondiente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicación del proveedor de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3797d02c67fc86ebfb44ff9e0e7b2c85cd1604206a58f1d8f5c3ca293599e92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404825"
---
# <a name="media-service-provider-communication"></a>Comunicación del proveedor de servicios multimedia

A partir Windows proveedores de servicios de telefonía 2000 que negocien una versión de 3.0 o posterior deben tener un proveedor de servicios multimedia correspondiente. La división precisa de las responsabilidades operativas depende de la implementación. Por ejemplo, un TSP podría usar el MSP correspondiente para realizar la determinación del tipo de medio en una sesión entrante. Sin embargo, el TSP debe ajustarse al TSPI, lo que significa obtener esa determinación del MSP y notificarlo a TAPI.

TSPI proporciona las siguientes funciones y mensajes para permitir una conexión virtual entre un TSP y un MSP:

-   [**Línea \_ TSPICloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**Línea \_ TSPICreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**Línea \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**Línea \_ TSPIReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**\_QOSINFO DE LÍNEA**](line-qosinfo.md)
-   [**LINE \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
