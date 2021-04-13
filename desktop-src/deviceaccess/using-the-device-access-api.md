---
title: Cómo usar la API de acceso a dispositivos
description: Este tema contiene tareas y consideraciones de diseño para usar la API de acceso a dispositivos.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 29c4812c559b691a896fb5bb9da39064bf3c8614
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421579"
---
# <a name="how-to-use-the-device-access-api"></a>Cómo usar la API de acceso a dispositivos

Este tema contiene tareas y consideraciones de diseño para usar la API de acceso a dispositivos.

## <a name="steps"></a>Pasos

| Tema | Descripción |
|---|---|
| [Consideraciones de diseño para dispositivos personalizados](design.md)<br/> | En este tema se describen las consideraciones de diseño que pueden ayudarle a determinar si el dispositivo necesita un controlador personalizado.<br/> |
| [Implementación del objeto de acceso del dispositivo](create-the-device-access-object.md)<br/> | En este tema se explica cómo crear una instancia del objeto de acceso del dispositivo y usarlo para tener acceso a un dispositivo. <br/>  |
| [Declarar la funcionalidad del dispositivo](declaring-the-device-capability.md)<br/> | En este tema se explica cómo declarar el GUID de la capacidad del dispositivo.<br/> |
| [Registro de la interfaz de dispositivo como restringido a las aplicaciones con privilegios](register-the-device-interface-class-as-privileged.md)<br/> | En este tema se muestra cómo agregar la propiedad **restringida** que indica que solo las aplicaciones con privilegios pueden acceder a una clase de interfaz de dispositivo.<br/> |
| [Creación de una extensión de Windows Runtime](create-a-windows-runtime-extension.md)<br/> | Puede crear un componente de Windows Runtime para encapsular el componente que tiene acceso al controlador. Después, puede escribir una aplicación de dispositivo de la tienda Windows para el dispositivo en C# o JavaScript.<br/> |

## <a name="additional-resources"></a>Recursos adicionales

- En el [ejemplo de acceso a controladores personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) se muestra cómo usar las API de acceso de dispositivos para tener acceso a un controlador personalizado desde una aplicación de dispositivo de la tienda Windows.
- [Aplicaciones de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) proporciona recursos para obtener más información sobre cómo diseñar y desarrollar aplicaciones de dispositivo de la tienda Windows para dispositivos especializados.
- El [centro de desarrollo de hardware](/windows-hardware/drivers/) proporciona recursos generales para las tareas de desarrollo de aplicaciones de dispositivo de la tienda Windows que son comunes a todos los tipos de dispositivos.
