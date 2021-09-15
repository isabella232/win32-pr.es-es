---
title: Consideraciones de diseño para dispositivos personalizados
description: En este tema se describen las consideraciones de diseño que pueden ayudarle a determinar si el dispositivo necesita un controlador personalizado.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570964"
---
# <a name="design-considerations-for-custom-devices"></a>Consideraciones de diseño para dispositivos personalizados

En este tema se describen las consideraciones de diseño que pueden ayudarle a determinar si el dispositivo necesita un controlador personalizado.

- [Determinar el tipo de controlador que se implementará](#determining-the-type-of-driver-to-implement)
- [Consideraciones de seguridad](#security-considerations)
- [Temas relacionados](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Determinar el tipo de controlador que se implementará

En esta tabla se describe cuándo debe desarrollar un controlador personalizado para el dispositivo y comunicarse con él mediante el API de acceso a dispositivos y cuándo debe usar en su lugar Windows pilas de dispositivos proporcionadas por el usuario.

| Para admitir | Implementación |
|:---|:---|
| Dispositivos conocidos, incluidos: <ul><li>Sensor</li><li>Location</li><li>Cámara web</li><li>Proximidad</li><li>Servicio de mensajes cortos (SMS)</li><li>Banda ancha móvil</li></ul><br/> | Para muchos tipos de dispositivos conocidos, no necesita un controlador personalizado, ya que Windows incluye API e interfaces de controlador de dispositivo (DDI) de extensión de clase que administran la comunicación entre el controlador y Windows. Sensor, ubicación y Windows dispositivos portátiles (WPD) son algunos ejemplos de clases de dispositivo que tienen esta compatibilidad. Si crea un controlador que usa uno de estos DDIs proporcionados por Windows para enviar y recibir datos y comandos, no es necesario que la aplicación Windows Store use el API de acceso a dispositivos para el acceso de agente o para enviar códigos de control de entrada/salida (E/S) directamente al controlador. <br/> Cuando una aplicación de Windows Store solicita acceso a un dispositivo conocido mediante la API de tiempo de ejecución de Windows para su clase de dispositivo, Windows 8 controlará el acceso a los dispositivos en función del tipo de dispositivo. Las aplicaciones siempre tendrán acceso a algunos tipos conocidos de dispositivos (como acelerómetros) que no revelan información de identificación personal. Otros tipos de dispositivos conocidos deben declararse en el manifiesto de aplicación para que una aplicación pueda acceder a ellos. El usuario debe conceder permiso para que una aplicación acceda a dispositivos que revelan información confidencial, como dispositivos de ubicación, cámara web y micrófono, o bien puede costar dinero al usuario, como los dispositivos de banda ancha móvil. <br/> |
| Un dispositivo WPD que implementa servicios MTP.<br/> | Puede usar el controlador de clase MTP o puede crear un controlador mediante el DDI de WPD.<br/> Windows 8 proporciona compatibilidad con los servicios de dispositivos MTP. Y una aplicación puede usar el [Windows. Devices.Portable](/uwp/api/Windows.Devices.Portable) Windows Runtime API, portable Device Component Object Model (COM) API o WPD Automation para acceder al dispositivo. La aplicación no necesita usar el API de acceso a dispositivos.<br/> |
| Un dispositivo que no tiene un controlador de clase Windows clase proporcionada por el usuario.<br/>  | En este caso, consulte las aplicaciones de dispositivos [UWP](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) para dispositivos internos para dispositivos especializados para determinar si debe implementar el acceso de controlador personalizado mediante el API de acceso a dispositivos.<br/> |

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En los artículos siguientes se proporcionan instrucciones para escribir código C++ seguro:

- [Procedimientos recomendados de seguridad para C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & Practices Security Guidance for Applications]/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso de controlador personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [aplicaciones de dispositivos UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de desarrollo de hardware](/windows-hardware/drivers/)
