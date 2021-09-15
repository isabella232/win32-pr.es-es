---
title: Uso de la API de acceso a dispositivos
description: Este tema contiene tareas y consideraciones de diseño para usar el API de acceso a dispositivos.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 29c4812c559b691a896fb5bb9da39064bf3c8614
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570929"
---
# <a name="how-to-use-the-device-access-api"></a>Uso de la API de acceso a dispositivos

Este tema contiene tareas y consideraciones de diseño para usar el API de acceso a dispositivos.

## <a name="steps"></a>Pasos

| Tema | Descripción |
|---|---|
| [Consideraciones de diseño para dispositivos personalizados](design.md)<br/> | En este tema se describen las consideraciones de diseño que pueden ayudarle a determinar si el dispositivo necesita un controlador personalizado.<br/> |
| [Implementar el objeto device access](create-the-device-access-object.md)<br/> | En este tema se explica cómo crear instancias del objeto de acceso del dispositivo y usarlo para acceder a un dispositivo. <br/>  |
| [Declarar la funcionalidad del dispositivo](declaring-the-device-capability.md)<br/> | En este tema se explica cómo declarar el GUID de funcionalidad del dispositivo.<br/> |
| [Registro de la interfaz del dispositivo como restringida a las aplicaciones con privilegios](register-the-device-interface-class-as-privileged.md)<br/> | En este tema se muestra cómo agregar la **propiedad Restricted** que indica que solo las aplicaciones con privilegios pueden acceder a una clase de interfaz de dispositivo.<br/> |
| [Creación de una extensión Windows runtime](create-a-windows-runtime-extension.md)<br/> | Puede crear un componente Windows runtime para encapsular el componente que tiene acceso al controlador. Después, puede escribir una aplicación Windows Store para el dispositivo en C# o JavaScript.<br/> |

## <a name="additional-resources"></a>Recursos adicionales

- El [ejemplo de acceso de controlador](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) personalizado muestra cómo usar las API de acceso a dispositivos para acceder a un controlador personalizado desde una Windows store.
- [Las aplicaciones de dispositivos UWP](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) para dispositivos internos proporcionan recursos para obtener más información sobre cómo diseñar y desarrollar aplicaciones de dispositivos Windows Store para dispositivos especializados.
- El [Centro de desarrollo de hardware](/windows-hardware/drivers/) proporciona recursos generales para las Windows desarrollo de aplicaciones de dispositivos de store que son comunes a todos los tipos de dispositivos.
