---
description: WIA se implementa como un servidor fuera de proceso del modelo de objetos componentes (COM) para garantizar el funcionamiento eficaz de las aplicaciones cliente.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Arquitectura WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563960"
---
# <a name="wia-architecture"></a>Arquitectura WIA

WIA se implementa como un servidor fuera de proceso del modelo de objetos componentes (COM) para garantizar el funcionamiento eficaz de las aplicaciones cliente. A diferencia de la mayoría de las aplicaciones de servidor de proceso, la adquisición de imágenes de Windows (WIA) evita penalizaciones de rendimiento durante la transferencia de datos de imagen al proporcionar su propio mecanismo de transferencia de datos, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer). Esta interfaz de alto rendimiento utiliza una ventana de memoria compartida para transferir datos al cliente.

WIA tiene tres componentes principales: un Administrador de dispositivos, una biblioteca de servicio de minicontrolador y un minicontrolador de dispositivo.

-   En el Administrador de dispositivos se enumeran los dispositivos de creación de imágenes, se recuperan las propiedades del dispositivo, se configuran los eventos de los dispositivos y se crean objetos de dispositivo.
-   La biblioteca de servicio de minicontrolador implementa todos los servicios que son independientes del dispositivo.
-   El minicontrolador de dispositivo asigna propiedades y comandos de WIA al dispositivo específico.

En el diagrama siguiente se ilustra la arquitectura de WIA:

![arquitectura WIA](images/wiarch.gif)

 

 



