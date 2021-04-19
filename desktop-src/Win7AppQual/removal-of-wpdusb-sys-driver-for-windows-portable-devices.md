---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Eliminación de WPDUSB.SYS controlador para dispositivos portátiles de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707117"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Eliminación de WPDUSB.SYS controlador para dispositivos portátiles de Windows

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

Microsoft ha reemplazado el componente de modo kernel de la pila de controladores USB (WPDUSB.SYS) de Windows Vista para dispositivos portátiles de Windows (WPD) con el controlador de WINUSB.SYS genérico. La comunicación con el controlador de WPDUSB.SYS original era a través de códigos de control de e/s privados (IOCTL). también se ha quitado la compatibilidad con estas.

Cualquier consumidor de estos códigos de IOCTL habría sido responsable de la interpretación y la implementación adecuadas del Protocolo de transferencia multimedia (MTP). Windows Vista no admitía el uso de estos códigos de IOCTL por parte de aplicaciones de terceros.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Cualquier aplicación que dependa de la disponibilidad de estos códigos de IOCTL privados ya no tendría acceso a los dispositivos MTP conectados con USB.

## <a name="mitigation"></a>Mitigación

Los usuarios de una aplicación que dependan de los códigos de IOCTL privados deben usar una aplicación diferente (o una versión actualizada de la aplicación) para tener acceso al dispositivo MTP conectado mediante USB.

## <a name="solution"></a>Solución

Las aplicaciones deben usar la API de dispositivos portátiles de Windows (WPD) para buscar e interactuar con cualquier dispositivo de WPD. Aunque un porcentaje significativo de los dispositivos WPD implementan MTP para la comunicación con el equipo, WPD no se limita únicamente a los dispositivos MTP. Además, cuando el acceso directo al dispositivo a través del ioctl privado habría limitado la aplicación a la comunicación solo con dispositivos conectados mediante USB, el uso de la API de WPD amplía la lista de opciones de conectividad a otros protocolos de comunicación (por ejemplo, Wi-Fi). En los casos excepcionales en los que la aplicación debe ser compatible con MTP, la API de WPD proporciona un mecanismo de paso a través para los comandos MTP sin procesar.

## <a name="leveraging-feature-capabilities"></a>Aprovechar las capacidades de características

La API de WPD es compatible con Windows XP (a través del SDK de formato de Windows), Windows Vista y Windows 7. La implementación de Windows 7 de WPD agrega compatibilidad con MTP a través de Bluetooth.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

[Dispositivos portátiles de Windows](../windows-portable-devices.md)

 

 
