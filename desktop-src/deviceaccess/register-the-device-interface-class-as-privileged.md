---
title: Registro de la interfaz del dispositivo como restringida a las aplicaciones con privilegios
description: En este tema se muestra cómo agregar la propiedad Restricted que indica que solo las aplicaciones con privilegios pueden acceder a una clase de interfaz de dispositivo.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 62bca034a2edab9b31267f14672b4821ca6569dead0fd645d98c52c234c24cb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029055"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registro de la interfaz del dispositivo como restringida a las aplicaciones con privilegios

A las aplicaciones se les deniega el acceso a la funcionalidad del controlador personalizado, a menos que se les concedan permisos a través de metadatos de dispositivo firmados. En este tema se muestra cómo agregar la **propiedad Restricted** que indica que solo las aplicaciones con privilegios pueden acceder a una clase de interfaz de dispositivo. Los controladores de dispositivo personalizados deben tener esta propiedad.

## <a name="instructions"></a>Instructions

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Establecimiento de la propiedad Restricted en un archivo de información (INF)

En la `InterfaceInstall32` sección , se registra el GUID de la clase de interfaz de dispositivo.

Las líneas de la **directiva AddProperty** establecen las propiedades de la clase de dispositivo. La segunda línea establece una propiedad personalizada en una categoría de propiedad personalizada. El GUID de categoría de propiedad es **14c83a99-0b3f-44b7-be4c-a178d3990564** y el identificador de propiedad **es 2**. El valor `Flags` de entrada opcional no está presente y el tipo es **17** (**DEVPROP_TYPE_BOOLEAN**). El valor de la propiedad es **1**.

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a>Comentarios

En lugar de **la directiva AddInterface,** el controlador también puede llamar a la rutina [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) para registrar la clase de interfaz de dispositivo.

También puede establecer la propiedad de interfaz restringida llamando a la [**rutina IoSetDeviceInterfacePropertyData.**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata)

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de acceso de controlador personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [aplicaciones de dispositivos UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de desarrollo de hardware](/windows-hardware/drivers/)
