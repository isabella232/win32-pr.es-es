---
description: La Windows adquisición de imágenes (WIA) es una API y una interfaz de controlador de dispositivo (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Acerca de Windows adquisición de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451305"
---
# <a name="about-windows-image-acquisition"></a>Acerca de Windows adquisición de imágenes

La Windows adquisición de imágenes (WIA) es una API y una interfaz de controlador de dispositivo (DDI). La API de WIA está diseñada para permitir que las aplicaciones:

-   Se ejecuta en un entorno estable y sólido.
-   Minimice los problemas de interoperabilidad.
-   Enumerar los dispositivos de adquisición de imágenes disponibles.
-   Cree conexiones a varios dispositivos simultáneamente.
-   Consulta las propiedades de los dispositivos de forma estándar y ampliable.
-   Adquirir datos de dispositivo mediante mecanismos de transferencia estándar y de alto rendimiento.
-   Mantener las propiedades de imagen entre transferencias de datos.
-   Recibir notificaciones de una amplia variedad de eventos de dispositivo.

WIADDI está diseñado para minimizar la cantidad de código que un proveedor de hardware debe escribir, a la vez que mantiene la flexibilidad para crear soluciones individuales. Esto se logra mediante:

-   Proporcionar una biblioteca de servicio de dispositivos estándar que realiza la mayoría de las operaciones del controlador.
-   Promover estándares de comunicaciones de dispositivos del sector para que un controlador WIA admita la mayoría de los dispositivos WIA. Por ejemplo, Protocolo de transferencia de imágenes (PTP).
-   Permitir que el controlador de dispositivo admita interfaces personalizadas, sin necesidad de que use la biblioteca de servicio de dispositivos estándar. Sin embargo, los controladores todavía necesitan implementar las interfaces WIA estándar.

En esta sección se presenta una breve introducción a la interfaz WIA en las áreas siguientes:

-   [Arquitectura de WIA](-wia-wia-architecture.md)
-   [Compatibilidad con ASS](-wia-sti-compatibility.md)
-   [Compatibilidad con T PLUGIN](-wia-twain-compatibility.md)
-   [WiA Administrador de dispositivos](-wia-wia-device-manager.md)
-   [Biblioteca del servicio WIA Minidriver](-wia-wia-minidriver-service-library.md)
-   [WIA Minidriver](-wia-wia-minidriver.md)

 

 



