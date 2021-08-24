---
title: 'Interfaces COM: acceso a dispositivos'
description: Interfaces del Modelo de objetos componentes (COM) en el API de acceso a dispositivos.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 22447151b944a2ac5515222eebd528fed11e2479d8a8c4db59e2da46dd07a130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793395"
---
# <a name="com-interfaces---device-access"></a>Interfaces COM: acceso a dispositivos

Interfaces del Modelo de objetos componentes (COM) en el API de acceso a dispositivos.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | La [**interfaz ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) se devuelve desde una llamada a CreateDeviceAccessInstance. Permite al autor de la llamada controlar la operación de enlace a una instancia de un dispositivo con el fin de recuperar otra interfaz que se puede usar para interactuar con ese dispositivo.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Envía un código de control a un controlador de dispositivo. Esta acción hace que el dispositivo realice la operación correspondiente. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Proporciona un método para controlar la finalización de llamadas al [**método DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)<br/> |

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso de controlador personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [aplicaciones de dispositivos UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de desarrollo de hardware](/windows-hardware/drivers/)
