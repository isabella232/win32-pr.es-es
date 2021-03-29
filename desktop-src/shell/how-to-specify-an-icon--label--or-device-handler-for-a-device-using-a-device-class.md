---
description: Las clases de dispositivo permiten la especificación de las propiedades Icons, Label y DeviceHandlers de cualquier dispositivo de esa clase.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante una clase de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997693"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a><span data-ttu-id="8bbac-103">Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante una clase de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8bbac-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>

<span data-ttu-id="8bbac-104">Las clases de dispositivo permiten la especificación de las propiedades Icons, Label y DeviceHandlers de cualquier dispositivo de esa clase.</span><span class="sxs-lookup"><span data-stu-id="8bbac-104">Device classes allow the specification of the Icons, Label, and DeviceHandlers properties for any device of that class.</span></span> <span data-ttu-id="8bbac-105">Esto es similar al uso de grupos de dispositivos, pero las clases de dispositivos y sus pertenencias vienen determinadas por el hardware en lugar de crearse o asignarse.</span><span class="sxs-lookup"><span data-stu-id="8bbac-105">This is similar to the use of device groups, but device classes and their memberships are determined by the hardware rather than being created or assigned.</span></span> <span data-ttu-id="8bbac-106">Cada nombre de clave de clase, que es el GUID de la interfaz de dispositivo Plug and Play, se encuentra en la clave **DeviceClasses** .</span><span class="sxs-lookup"><span data-stu-id="8bbac-106">Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key.</span></span> <span data-ttu-id="8bbac-107">En la clave de clase individual, asigne los valores de iconos, etiqueta y DeviceHandlers.</span><span class="sxs-lookup"><span data-stu-id="8bbac-107">Under the individual class key, assign the values for Icons, Label, and DeviceHandlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="8bbac-108">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="8bbac-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8bbac-109">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="8bbac-109">Step 1:</span></span>

<span data-ttu-id="8bbac-110">En el ejemplo siguiente se muestra la clave de clase y los valores de DeviceHandlers para la interfaz de volumen.</span><span class="sxs-lookup"><span data-stu-id="8bbac-110">The following example shows the class key and DeviceHandlers values for the volume interface.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

<span data-ttu-id="8bbac-111">También puede Agregar propiedades de dispositivo personalizadas en la clave de clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bbac-111">You can also add custom device properties under the device class key.</span></span> <span data-ttu-id="8bbac-112">Las propiedades del dispositivo personalizado se aplican a todos los dispositivos de esa clase.</span><span class="sxs-lookup"><span data-stu-id="8bbac-112">The custom device properties then apply to all devices in that class.</span></span> <span data-ttu-id="8bbac-113">Los dispositivos y los controladores de dispositivo siempre deben tener asociados iconos y etiquetas para cumplir los requisitos mínimos de uso.</span><span class="sxs-lookup"><span data-stu-id="8bbac-113">Devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

> [!Note]  
> <span data-ttu-id="8bbac-114">Las propiedades que se definen en el nivel de instancia de dispositivo tienen prioridad sobre las propiedades definidas en el nivel de grupo de dispositivos, que a su vez tienen prioridad sobre las propiedades definidas en el nivel de clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bbac-114">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



