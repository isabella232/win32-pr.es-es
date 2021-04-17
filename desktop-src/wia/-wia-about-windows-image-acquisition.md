---
description: La interfaz de adquisición de imágenes de Windows (WIA) es una API y una interfaz de controlador de dispositivo (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Acerca de la adquisición de imágenes de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716063"
---
# <a name="about-windows-image-acquisition"></a>Acerca de la adquisición de imágenes de Windows

La interfaz de adquisición de imágenes de Windows (WIA) es una API y una interfaz de controlador de dispositivo (DDI). La API de WIA está diseñada para permitir a las aplicaciones:

-   Ejecutarse en un entorno sólido y estable.
-   Minimice los problemas de interoperabilidad.
-   Enumera los dispositivos de adquisición de imágenes disponibles.
-   Cree conexiones a varios dispositivos simultáneamente.
-   Consultar las propiedades de los dispositivos de forma estándar y ampliable.
-   Adquirir datos del dispositivo mediante mecanismos de transferencia estándar y de alto rendimiento.
-   Mantener las propiedades de la imagen entre las transferencias de datos.
-   Recibir una notificación de una amplia variedad de eventos de dispositivo.

WIADDI está diseñado para minimizar la cantidad de código que un proveedor de hardware debe escribir, a la vez que mantiene la flexibilidad de crear soluciones individuales. Esto se logra mediante:

-   Proporcionar una biblioteca de servicio de dispositivo estándar que realiza la mayoría de las operaciones de controlador.
-   Promoción de los estándares de comunicación de dispositivos de la industria para que un controlador WIA admita la mayoría de los dispositivos WIA. Por ejemplo, el protocolo de transferencia de imágenes (PTP).
-   Permite que el controlador de dispositivo admita interfaces personalizadas, pero no requiere que use la biblioteca de servicio de dispositivo estándar. Sin embargo, los controladores todavía necesitan implementar las interfaces estándar de WIA.

En esta sección se presenta una breve introducción a la interfaz WIA en las siguientes áreas:

-   [Arquitectura WIA](-wia-wia-architecture.md)
-   [Compatibilidad de STI](-wia-sti-compatibility.md)
-   [Compatibilidad con TWAIN](-wia-twain-compatibility.md)
-   [Administrador de dispositivos WIA](-wia-wia-device-manager.md)
-   [Biblioteca de servicio minicontrolador de WIA](-wia-wia-minidriver-service-library.md)
-   [Minicontrolador WIA](-wia-wia-minidriver.md)

 

 



