---
description: Eliminación de WPDUSB.SYS Driver for Windows Portable Devices
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Eliminación de WPDUSB.SYS Driver for Windows Portable Devices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b5d1a815b97049816a618b9e93d0767e321fd60b689e6845318c1605574c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994745"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Eliminación de WPDUSB.SYS Driver for Windows Portable Devices

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

Microsoft ha reemplazado el componente de modo kernel de la pila de controladores USB de Windows Vista (WPDUSB.SYS) para Windows Portable Devices (WPD) por el controlador WINUSB.SYS genérico. La comunicación con el controlador WPDUSB.SYS era a través de códigos privados de control de E/S (IOCTL). también se ha quitado la compatibilidad de estos.

Cualquier consumidor de estos códigos IOCTL habría sido responsable de la correcta interpretación e implementación del Protocolo de transferencia de medios (MTP). Windows Vista no admite el uso de estos códigos IOCTL por parte de aplicaciones de terceros.

## <a name="manifestation-of-impact"></a>Demostración de impacto

Cualquier aplicación que dependiera de la disponibilidad de estos códigos IOCTL privados ya no tendría acceso a los dispositivos MTP conectados a USB.

## <a name="mitigation"></a>Mitigación

Los usuarios de una aplicación que depende de los códigos IOCTL privados deben usar una aplicación diferente (o una versión actualizada de la aplicación) para acceder al dispositivo MTP conectado a USB.

## <a name="solution"></a>Solución

Las aplicaciones deben usar Windows API de dispositivos portátiles (WPD) para buscar e interactuar con cualquier dispositivo WPD. Aunque un porcentaje significativo de dispositivos WPD implementan MTP para la comunicación con el equipo, WPD no se limita solo a los dispositivos MTP. Además, si el acceso directo al dispositivo a través de las ICTL privadas hubiera limitado la aplicación a la comunicación solo con dispositivos conectados a USB, el uso de la API de WPD amplía la lista de opciones de conectividad a otros protocolos de comunicación (por ejemplo, Wi-Fi). En los casos excepcionales en los que la aplicación debe tener en cuenta MTP, la API de WPD proporciona un mecanismo de paso a través para los comandos de MTP sin procesar.

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

La API de WPD se admite en Windows XP (a través del SDK Windows Format), Windows Vista y Windows 7. La Windows 7 de WPD agrega compatibilidad con MTP en Bluetooth.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

[Windows Dispositivos portátiles](../windows-portable-devices.md)

 

 
