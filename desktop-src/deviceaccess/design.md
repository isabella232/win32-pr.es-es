---
title: Consideraciones de diseño para dispositivos personalizados
description: En este tema se describen las consideraciones de diseño que pueden ayudarle a determinar si el dispositivo necesita un controlador personalizado.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797188"
---
# <a name="design-considerations-for-custom-devices"></a>Consideraciones de diseño para dispositivos personalizados

En este tema se describen las consideraciones de diseño que pueden ayudarle a determinar si el dispositivo necesita un controlador personalizado.

- [Determinar el tipo de controlador que se va a implementar](#determining-the-type-of-driver-to-implement)
- [Consideraciones de seguridad](#security-considerations)
- [Temas relacionados](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Determinar el tipo de controlador que se va a implementar

En esta tabla se describe cuándo se debe desarrollar un controlador personalizado para el dispositivo y comunicarse con él mediante la API de acceso de dispositivos y, en su lugar, usar pilas de dispositivos proporcionados por Windows.

| Para admitir | Implementación |
|:---|:---|
| Dispositivos conocidos, incluidos: <ul><li>Sensor</li><li>Ubicación</li><li>Cámara web</li><li>Proximidad</li><li>Servicio de mensajes cortos (SMS)</li><li>Banda ancha móvil</li></ul><br/> | Para muchos tipos de dispositivos conocidos, no se necesita un controlador personalizado, ya que Windows incluye las API y las interfaces de controlador de dispositivo de extensión de clase (DDIs) que administran la comunicación entre el controlador y Windows. Los dispositivos de sensor, ubicación y dispositivo portátil de Windows (WPD) son algunos ejemplos de clases de dispositivos que tienen esta compatibilidad. Si compila un controlador que usa uno de estos DDIs proporcionados por Windows para enviar y recibir datos y comandos, no es necesario que la aplicación de la tienda Windows use la API de acceso de dispositivos para el acceso al agente o envíe códigos de control de entrada/salida (e/s) directamente al controlador. <br/> Cuando una aplicación de la tienda Windows solicita acceso a un dispositivo conocido mediante el uso de la API de Windows Runtime para su clase de dispositivo, Windows 8 controlará el acceso de los dispositivos en función del tipo de dispositivo. Las aplicaciones siempre obtendrán acceso a algunos tipos conocidos de dispositivos (como los acelerómetros) que no revelan ninguna información de identificación personal. Otros tipos de dispositivos conocidos se deben declarar en el manifiesto de aplicación para que una aplicación pueda acceder a ellos. El usuario debe conceder permiso para que una aplicación tenga acceso a los dispositivos que revelen información confidencial, como la ubicación, la cámara web y los dispositivos de micrófono, o pueden costar el dinero del usuario, como los dispositivos de banda ancha móvil. <br/> |
| Un dispositivo de WPD que implementa los servicios MTP.<br/> | Puede usar el controlador de la clase MTP o puede compilar un controlador mediante el DDI WPD.<br/> Windows 8 proporciona compatibilidad con los servicios de dispositivos MTP. Además, una aplicación puede usar la API [Windows. Devices. Portable](/uwp/api/Windows.Devices.Portable) Windows Runtime, la API del modelo de objetos componentes (com) de dispositivo portátil o la automatización WPD para tener acceso al dispositivo. No es necesario que la aplicación use la API de acceso a dispositivos.<br/> |
| Un dispositivo que no tiene una extensión de clase o controlador de clase proporcionados por Windows.<br/>  | En este caso, consulte las [aplicaciones de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) para dispositivos especializados con el fin de determinar si debe implementar el acceso a los controladores personalizados mediante la API de acceso a dispositivos.<br/> |

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En los artículos siguientes se proporcionan instrucciones para escribir código de C++ seguro:

- [Prácticas recomendadas de seguridad para C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & guía de seguridad para aplicaciones]/Previous-Versions/MSP-n-p/ff650760 (v = pandp. 10))

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso a controladores personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicaciones para dispositivos UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desarrollo de hardware](/windows-hardware/drivers/)
