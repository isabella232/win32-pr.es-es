---
title: Declarar la funcionalidad del dispositivo
description: En este tema se explica cómo declarar el GUID de funcionalidad del dispositivo.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570968"
---
# <a name="declaring-the-device-capability"></a>Declarar la funcionalidad del dispositivo

En este tema se explica cómo declarar el GUID de funcionalidad del dispositivo. Todas las aplicaciones que tienen como destino controladores personalizados deben declarar esta funcionalidad.

En el manifiesto de aplicación, deberá agregar una funcionalidad de dispositivo, como se muestra a continuación:

Este es un ejemplo de una declaración de funcionalidad para un dispositivo personalizado. El GUID es el GUID de la clase de interfaz de dispositivo.

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso de controlador personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [aplicaciones de dispositivos UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de desarrollo de hardware](/windows-hardware/drivers/)
