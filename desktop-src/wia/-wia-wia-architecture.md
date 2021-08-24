---
description: WIA se implementa como un servidor fuera de proceso del Modelo de objetos componentes (COM) para garantizar el funcionamiento sólido de las aplicaciones cliente.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Arquitectura de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a6bb88fba5a79f2915500786bbfcf8d531bfe0170ec6c6841f419425ee296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813274"
---
# <a name="wia-architecture"></a>Arquitectura de WIA

WIA se implementa como un servidor fuera de proceso del Modelo de objetos componentes (COM) para garantizar el funcionamiento sólido de las aplicaciones cliente. A diferencia de la mayoría de las aplicaciones de servidor de procesos, Windows Image Acquisition (WIA) evita las penalizaciones de rendimiento durante la transferencia de datos de imagen al proporcionar su propio mecanismo de transferencia de datos, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer). Esta interfaz de alto rendimiento usa una ventana de memoria compartida para transferir datos al cliente.

WIA tiene tres componentes principales: un Administrador de dispositivos, una biblioteca de servicios de Minidriver y un minidriver de dispositivo.

-   El Administrador de dispositivos enumera los dispositivos de creación de imágenes, recupera las propiedades del dispositivo, configura eventos para los dispositivos y crea objetos de dispositivo.
-   La biblioteca de servicios de Minidriver implementa todos los servicios que son independientes del dispositivo.
-   Device Minidriver asigna propiedades y comandos de WIA al dispositivo específico.

En el diagrama siguiente se muestra la arquitectura de WIA:

![arquitectura wia](images/wiarch.gif)

 

 



