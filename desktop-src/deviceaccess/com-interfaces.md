---
title: 'Interfaces COM: acceso a dispositivos'
description: Interfaces del modelo de objetos componentes (COM) en el API de acceso a dispositivos.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570977"
---
# <a name="com-interfaces---device-access"></a>Interfaces COM: acceso a dispositivos

Interfaces del modelo de objetos componentes (COM) en el API de acceso a dispositivos.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | La [**interfaz ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) se devuelve desde una llamada a CreateDeviceAccessInstance. Permite al autor de la llamada controlar la operación de enlace a una instancia de un dispositivo con el fin de recuperar otra interfaz que se puede usar para interactuar con ese dispositivo.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Envía un código de control a un controlador de dispositivo. Esta acción hace que el dispositivo realice la operación correspondiente. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Proporciona un método para controlar la finalización de llamadas al [**método DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)<br/> |

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso de controlador personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [aplicaciones de dispositivos UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de desarrollo de hardware](/windows-hardware/drivers/)
