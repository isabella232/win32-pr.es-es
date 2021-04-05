---
title: Registro de la interfaz de dispositivo como restringido a las aplicaciones con privilegios
description: En este tema se muestra cómo agregar la propiedad restringida que indica que solo las aplicaciones con privilegios pueden acceder a una clase de interfaz de dispositivo.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078566"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="2b7d5-103">Registro de la interfaz de dispositivo como restringido a las aplicaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="2b7d5-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="2b7d5-104">A las aplicaciones se les deniega el acceso a la funcionalidad del controlador personalizado, a menos que se les concedan permisos mediante metadatos de dispositivo firmados</span><span class="sxs-lookup"><span data-stu-id="2b7d5-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="2b7d5-105">En este tema se muestra cómo agregar la propiedad **restringida** que indica que solo las aplicaciones con privilegios pueden acceder a una clase de interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="2b7d5-106">Los controladores de dispositivos personalizados deben tener esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="2b7d5-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="2b7d5-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="2b7d5-108">Establecer la propiedad Restricted en un archivo de información (INF)</span><span class="sxs-lookup"><span data-stu-id="2b7d5-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="2b7d5-109">En la `InterfaceInstall32` sección, se registra el GUID de la clase de interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="2b7d5-110">Las líneas de la directiva **AddProperty** establecen las propiedades de la clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="2b7d5-111">La segunda línea establece una propiedad personalizada en una categoría de propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="2b7d5-112">El GUID de categoría de propiedad es **14c83a99-0b3f-44b7-be4c-a178d3990564** y el identificador de propiedad es **2**.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="2b7d5-113">El `Flags` valor de entrada opcional no está presente y el tipo es **17** (**DEVPROP_TYPE_BOOLEAN**).</span><span class="sxs-lookup"><span data-stu-id="2b7d5-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="2b7d5-114">El valor de la propiedad es **1**.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-114">The value of the property is **1**.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="2b7d5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b7d5-115">Remarks</span></span>

<span data-ttu-id="2b7d5-116">En lugar de la directiva **AddInterface** , el controlador también puede llamar a la rutina [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) para registrar la clase de interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b7d5-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="2b7d5-117">También puede establecer la propiedad de interfaz restringida llamando a la rutina [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .</span><span class="sxs-lookup"><span data-stu-id="2b7d5-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b7d5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b7d5-118">Related topics</span></span>

<span data-ttu-id="2b7d5-119">[Ejemplo de acceso a controladores personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicaciones para dispositivos UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desarrollo de hardware](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="2b7d5-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
