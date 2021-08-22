---
title: Acerca de la API de acceso a dispositivos
description: La API de acceso a dispositivos es para los desarrolladores de C++ que crean una aplicación de Windows Store para interactuar con dispositivos especializados en Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 08d603e74ff33250bbc5a65e440fc47a0103cd6eb996badf94dbdc51b6b2d3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755025"
---
# <a name="about-the-device-access-api"></a>Acerca de la API de acceso a dispositivos

La API de acceso a dispositivos es para los desarrolladores de C++ que crean una aplicación de Windows Store para interactuar con dispositivos especializados en Windows 8. En este tema se describen los escenarios a los que se API de acceso a dispositivos aplicación. También se explica cómo el API de acceso a dispositivos las reglas de seguridad para las Windows Store en Windows 8.

- [Habilitación de la funcionalidad de dispositivo personalizada en Windows store](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Habilitación de la funcionalidad de dispositivo personalizada en Windows store

Los desarrolladores de fabricantes de hardware independientes (IHV) y OEM pueden compilar una aplicación de Windows Store que se empareja con su dispositivo y que se adquiere automáticamente cuando se instala el dispositivo. Esta aplicación, conocida como aplicación Windows store, puede proporcionar una funcionalidad de dispositivo única.

Los dispositivos que no tienen controladores de clase integrados ni API de runtime Windows para comunicarse con el dispositivo en Windows 8 se conocen como dispositivos *especializados.* Estos dispositivos pueden requerir un controlador personalizado. Para obtener más información sobre los tipos de dispositivos que requieren controladores personalizados, consulte la guía de diseño de aplicaciones de dispositivos de Windows Store para dispositivos especializados.

La aplicación de dispositivo de Windows Store para un dispositivo especializado que debe comunicarse con el controlador personalizado de un dispositivo no puede usar las API de Microsoft Win32 como [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) y [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) para enviar ICTLs al dispositivo. El entorno de seguridad restringido en el que Windows aplicaciones de dispositivo de la Tienda requieren que use el API de acceso a dispositivos para comunicarse con el controlador personalizado desde una aplicación de Windows Store.

El desarrollador de un dispositivo personalizado restringe el acceso a aplicaciones con privilegios aprobadas. Por ejemplo, es posible que el fabricante de un dispositivo de reproductor multimedia quiera que los usuarios solo puedan reproducir música a través de la aplicación de música proporcionada por IHV y impedir que cualquier aplicación de la competencia sincronice los medios desde el dispositivo. Al compilar el controlador de dispositivo, establezca una propiedad en el archivo de información (INF) para especificar que solo las aplicaciones con privilegios puedan acceder al dispositivo. Los metadatos del propio dispositivo especifican los ID de paquete para el conjunto de aplicaciones aprobadas. Consulta [Aplicaciones de dispositivos UWP para dispositivos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) internos para obtener más detalles sobre el proceso de establecer estos metadatos en el dispositivo.

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso de controlador personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [aplicaciones de dispositivos UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de desarrollo de hardware](/windows-hardware/drivers/)