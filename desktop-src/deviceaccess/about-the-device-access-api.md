---
title: Acerca de la API de acceso a dispositivos
description: La API de acceso a dispositivos es para desarrolladores de C++ que crean una aplicación de la tienda Windows para interactuar con dispositivos especializados en Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104359505"
---
# <a name="about-the-device-access-api"></a>Acerca de la API de acceso a dispositivos

La API de acceso a dispositivos es para desarrolladores de C++ que crean una aplicación de la tienda Windows para interactuar con dispositivos especializados en Windows 8. En este tema se describen los escenarios a los que se aplica la API de acceso a dispositivos. También se explica cómo la API de acceso a dispositivos aplica las reglas de seguridad para las aplicaciones de la tienda Windows en Windows 8.

- [Habilitar la funcionalidad de dispositivo personalizada en aplicaciones de dispositivo de la tienda Windows](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Habilitar la funcionalidad de dispositivo personalizada en aplicaciones de dispositivo de la tienda Windows

Los desarrolladores de proveedores de hardware independientes (IHV) y OEM pueden compilar una aplicación de la tienda Windows que se empareja con su dispositivo y se adquiere automáticamente al instalar el dispositivo. Esta aplicación, conocida como una aplicación de dispositivo de la tienda Windows, puede proporcionar una funcionalidad de dispositivo única.

Los dispositivos que no tienen controladores de clase integrados o API de Windows Runtime para comunicarse con el dispositivo en Windows 8 se conocen como *dispositivos especializados*. Estos dispositivos pueden requerir un controlador personalizado. Para obtener más información acerca de los tipos de dispositivos que requieren controladores personalizados, consulte la guía de diseño de aplicaciones de dispositivos de la tienda Windows para dispositivos especializados.

La aplicación de dispositivo de la tienda Windows para un dispositivo especializado que debe comunicarse con el controlador personalizado de un dispositivo no puede usar las API de Microsoft Win32 como [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) y [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) para enviar IOCTL al dispositivo. El entorno de seguridad restringido donde se ejecutan las aplicaciones de dispositivo de la tienda Windows requiere que use la API de acceso de dispositivos para comunicarse con el controlador personalizado desde una aplicación de la tienda Windows.

El desarrollador de un dispositivo personalizado restringe el acceso a aplicaciones aprobadas y con privilegios. Por ejemplo, el fabricante de un dispositivo de Media-Player podría querer que los usuarios reproduzcan música solo a través de la aplicación de música proporcionada por IHV y restrinjan la sincronización de la aplicación de los medios desde el dispositivo. Al compilar el controlador de dispositivo, se establece una propiedad en el archivo de información (INF) para especificar que solo las aplicaciones con privilegios puedan tener acceso al dispositivo. Los metadatos del propio dispositivo especifican los identificadores de paquete para el conjunto de aplicaciones aprobadas. Para obtener más información sobre el proceso de configuración de estos metadatos en el dispositivo, vea [aplicaciones de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) .

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso a controladores personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicaciones para dispositivos UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desarrollo de hardware](/windows-hardware/drivers/)