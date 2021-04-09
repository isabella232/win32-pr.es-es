---
title: Acerca de Bluetooth
description: Bluetooth es un protocolo estándar del sector que habilita la conectividad inalámbrica para una multitud de dispositivos, incluidos equipos, impresoras, teléfonos móviles y dispositivos de mano.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, descrito
- Bluetooth Bluetooth, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077363"
---
# <a name="about-bluetooth"></a>Acerca de Bluetooth

Bluetooth es un protocolo estándar del sector que habilita la conectividad inalámbrica para una multitud de dispositivos, incluidos equipos, impresoras, teléfonos móviles y dispositivos de mano.

Las características clave de Bluetooth incluyen:

-   Un protocolo inalámbrico de bajo coste y bajo consumo de energía con soporte técnico estándar del sector y aceptación mundial.
-   Una interfaz de programación definida y familiar que los desarrolladores pueden usar para desarrollar o migrar aplicaciones rápidamente.
-   Un sitio web oficial y una organización cooperativa en todo el sector que explica, promueve y normaliza la tecnología Bluetooth. Para obtener más información, vea [www.Bluetooth.com](https://www.bluetooth.com/).

Bluetooth en Windows proporciona servicios principales que son similares a los expuestos por el protocolo de control de transmisión (la parte TCP de TCP/IP). Como muchos protocolos y servicios de red, la conectividad Bluetooth y la transferencia de datos se programan a través de llamadas a funciones de Windows Sockets, mediante las técnicas de programación de Windows Sockets comunes y las extensiones de Bluetooth específicas. Sin embargo, dado que existen diferencias significativas entre una red cableada, fija y una red ad hoc inalámbrica, Bluetooth proporciona extensiones como detección de servicio/dispositivo y notificación que permiten que las aplicaciones funcionen correctamente en el entorno inalámbrico. Estas extensiones también disponen de la forma de portabilidad simple a tecnologías similares, como IrDA, o transportes inalámbricos futuros.

Microsoft ofrece compatibilidad con Bluetooth en Windows XP con Service Pack 1 (SP1) y versiones posteriores, en Windows XP Embedded con Service Pack 2 y en Windows CE. Las aplicaciones Bluetooth que se ejecutan en Windows XP deben poder ejecutarse en una imagen de tiempo de ejecución basada en Windows XP Embedded que incluye las dependencias requeridas. Para obtener más información acerca de Windows XP Embedded, consulte la documentación de la ayuda de Windows XP Embedded en MSDN. Para obtener más información acerca de la programación de Windows CE, consulte el SDK de Windows CE.

Microsoft proporciona dos métodos para programar Bluetooth en Windows:

-   Usar la interfaz de Windows Sockets
-   Administración directa de dispositivos mediante interfaces Bluetooth que no son de socket

En esta sección se proporciona información general sobre ambos enfoques en los temas siguientes. Para obtener más información sobre el uso de elementos de la API de Windows Sockets para programar Bluetooth, consulte [programación de Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md).



| Sección                                                                                | Contenido                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Compatibilidad de Windows Sockets con Bluetooth](windows-sockets-support-for-bluetooth.md)     | Describe la relación entre Bluetooth y Windows Sockets. |
| [Administración de dispositivos y servicios Bluetooth](managing-bluetooth-devices-and-services.md) | Describe cómo administrar dispositivos y servicios Bluetooth.           |



 

 

 




