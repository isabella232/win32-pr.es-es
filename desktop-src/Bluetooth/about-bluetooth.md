---
title: Acerca de Bluetooth
description: Bluetooth es un protocolo estándar del sector que permite la conectividad inalámbrica para una gran cantidad de dispositivos, incluidos equipos, impresoras, teléfonos móviles y dispositivos portátiles.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth , descrito
- Bluetooth Bluetooth , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974630"
---
# <a name="about-bluetooth"></a>Acerca de Bluetooth

Bluetooth es un protocolo estándar del sector que permite la conectividad inalámbrica para una gran cantidad de dispositivos, incluidos equipos, impresoras, teléfonos móviles y dispositivos portátiles.

Entre las Bluetooth principales se incluyen:

-   Un protocolo inalámbrico de bajo costo y bajo consumo de energía con soporte estándar del sector y aceptación mundial.
-   Interfaz de programación definida y familiar que los desarrolladores pueden usar para desarrollar o portabilidad rápidamente aplicaciones.
-   Un sitio web oficial y una organización cooperativa de todo el sector que explica, promueve y normaliza Bluetooth tecnología. Para obtener más información, [vea www.bluetooth.com](https://www.bluetooth.com/).

Bluetooth en Windows proporciona servicios principales similares a los expuestos por el Protocolo de control de transmisión (la parte TCP de TCP/IP). Al igual que muchos protocolos y servicios de red, la conectividad Bluetooth y la transferencia de datos se programan a través de llamadas de función de sockets de Windows, mediante técnicas comunes de programación de sockets de Windows y extensiones de Bluetooth específicas. Sin embargo, dado que existen diferencias significativas entre una red cableada fija y una red ad hoc inalámbrica, Bluetooth proporciona extensiones como la detección de servicios o dispositivos y la notificación que permiten que las aplicaciones funcionen correctamente en el entorno inalámbrico. Estas extensiones también allanan el camino para la porción sencilla a tecnologías similares, como IrDA o futuros transportes inalámbricos.

Microsoft proporciona compatibilidad con Bluetooth en Windows XP con Service Pack 1 (SP1) y versiones posteriores, en Windows XP Embedded con Service Pack 2 y en Windows CE. Bluetooth aplicaciones que se ejecutan en Windows XP deben poder ejecutarse en una imagen en tiempo de ejecución basada en Windows XP Embedded que incluya las dependencias necesarias. Para obtener más información sobre Windows XP Embedded, consulte la documentación Windows ayuda de XP Embedded en MSDN. Para obtener más información sobre Windows CE programación, consulte el SDK Windows CE.

Microsoft proporciona dos enfoques para programar Bluetooth en Windows:

-   Uso de la interfaz Windows Sockets
-   Administración directa de dispositivos mediante interfaces no Bluetooth cket

En esta sección se proporciona información general sobre ambos enfoques en los temas siguientes. Para obtener más información sobre el uso de Windows DE SOCKETS para programar Bluetooth, vea Programación Bluetooth con [sockets Windows sockets](bluetooth-programming-with-windows-sockets.md).



| Sección                                                                                | Contenido                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Compatibilidad de Windows Sockets con Bluetooth](windows-sockets-support-for-bluetooth.md)     | Describe la relación entre Bluetooth y Windows sockets. |
| [Administración Bluetooth dispositivos y servicios](managing-bluetooth-devices-and-services.md) | Describe cómo administrar Bluetooth dispositivos y servicios.           |



 

 

 




