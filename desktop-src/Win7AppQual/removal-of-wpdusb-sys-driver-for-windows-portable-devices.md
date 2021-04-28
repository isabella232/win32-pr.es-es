---
description: Eliminación de WPDUSB.SYS driver for Windows Portable Devices
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Eliminación de WPDUSB.SYS driver for Windows Portable Devices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116253"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Eliminación de WPDUSB.SYS driver for Windows Portable Devices

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

Microsoft ha reemplazado el componente de modo kernel de la pila de controladores USB de Windows Vista (WPDUSB.SYS) para dispositivos portátiles de Windows (WPD) por el controlador WINUSB.SYS genérico. La comunicación con el controlador WPDUSB.SYS era a través de códigos privados de control de E/S (IOCTL); También se ha quitado la compatibilidad de estos.

Cualquier consumidor de estos códigos IOCTL habría sido responsable de la correcta interpretación e implementación del Protocolo de transferencia de medios (MTP). Windows Vista no admite el uso de estos códigos IOCTL por parte de aplicaciones de terceros.

## <a name="manifestation-of-impact"></a>Demostración del impacto

Cualquier aplicación que dependiera de la disponibilidad de estos códigos IOCTL privados ya no tendría acceso a los dispositivos MTP conectados a USB.

## <a name="mitigation"></a>Mitigación

Los usuarios de una aplicación que dependa de los códigos IOCTL privados deben usar una aplicación diferente (o una versión actualizada de la aplicación) para acceder al dispositivo MTP conectado a USB.

## <a name="solution"></a>Solución

Las aplicaciones deben usar la API de dispositivos portátiles de Windows (WPD) para buscar e interactuar con cualquier dispositivo WPD. Aunque un porcentaje significativo de dispositivos WPD implementan MTP para la comunicación con el equipo, WPD no se limita solo a los dispositivos MTP. Además, cuando el acceso directo al dispositivo a través de las ICTL privadas habría limitado la aplicación a la comunicación solo con dispositivos conectados mediante USB, el uso de la API de WPD amplía la lista de opciones de conectividad a otros protocolos de comunicación (por ejemplo, Wi-Fi). En los casos poco frecuentes en los que la aplicación debe tener en cuenta MTP, la API de WPD proporciona un mecanismo de paso a través para los comandos MTP sin procesar.

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

La API de WPD se admite en Windows XP (a través del SDK de Windows Format), Windows Vista y Windows 7. La implementación de Windows 7 de WPD agrega compatibilidad con MTP a través de Bluetooth.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

[Dispositivos portátiles Windows](../windows-portable-devices.md)

 

 
