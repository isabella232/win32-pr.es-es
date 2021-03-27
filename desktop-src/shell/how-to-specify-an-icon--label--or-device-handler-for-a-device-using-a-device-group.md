---
description: Los grupos de dispositivos permiten la especificación de las propiedades Icons, Label o DeviceHandlers de cualquier dispositivo que declare parte de ese grupo.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante un grupo de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001902"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a><span data-ttu-id="41d29-103">Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante un grupo de dispositivos</span><span class="sxs-lookup"><span data-stu-id="41d29-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>

<span data-ttu-id="41d29-104">Los grupos de dispositivos permiten la especificación de las propiedades Icons, Label o DeviceHandlers de cualquier dispositivo que declare parte de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="41d29-104">Device groups allow the specification of the Icons, Label, or DeviceHandlers properties for any device that declares itself part of that group.</span></span> <span data-ttu-id="41d29-105">Si el grupo de dispositivos no es un grupo de dispositivos proporcionado por el sistema, se agregará una clave que defina el grupo de dispositivos en la clave **AutoplayHandlers** \\ **DeviceGroups** .</span><span class="sxs-lookup"><span data-stu-id="41d29-105">If the device group is not a system-provided device group, a key that defines the device group will be added under the **AutoplayHandlers**\\**DeviceGroups** key.</span></span> <span data-ttu-id="41d29-106">No es necesario establecer las tres propiedades de cada grupo; solo puede establecer las propiedades que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="41d29-106">You do not need to set all three properties for each group; you can set only those properties that you want to customize.</span></span> <span data-ttu-id="41d29-107">Sin embargo, los dispositivos y los controladores de dispositivo siempre deben tener asociados iconos y etiquetas para cumplir los requisitos mínimos de uso.</span><span class="sxs-lookup"><span data-stu-id="41d29-107">However, devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

## <a name="instructions"></a><span data-ttu-id="41d29-108">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="41d29-108">Instructions</span></span>


<span data-ttu-id="41d29-109">En el ejemplo siguiente se usa un sistema con varias unidades Zip conectadas.</span><span class="sxs-lookup"><span data-stu-id="41d29-109">The following example uses a system with several attached Zip drives.</span></span> <span data-ttu-id="41d29-110">Sin especificar los valores iconos, etiqueta y DeviceHandlers de cada unidad individualmente, se crea un grupo de dispositivos denominado ZipDrive y se definen los valores que contiene.</span><span class="sxs-lookup"><span data-stu-id="41d29-110">Without specifying the Icons, Label, and DeviceHandlers values for each drive individually, you create a device group called ZipDrive and define those values within it.</span></span> <span data-ttu-id="41d29-111">Cada unidad Zip se declara a continuación como un miembro del grupo ZipDrive.</span><span class="sxs-lookup"><span data-stu-id="41d29-111">Each Zip drive is then declared a member of the ZipDrive group.</span></span>

<span data-ttu-id="41d29-112">En primer lugar, defina el grupo de dispositivos agregando la siguiente clave *ZipDrive* y sus valores.</span><span class="sxs-lookup"><span data-stu-id="41d29-112">First, define the device group by adding the following *ZipDrive* key and its values.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

<span data-ttu-id="41d29-113">Cada dispositivo de unidad Zip se declara como parte del grupo ZipDrive, heredando las propiedades de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="41d29-113">Each Zip drive device is then declared as part of the ZipDrive group, inheriting the properties of that group.</span></span> <span data-ttu-id="41d29-114">En la clave **DeviceParameters** de la instancia del dispositivo, agregue un valor denominado DeviceGroup como tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="41d29-114">Under the **DeviceParameters** key of the device instance, add a value named DeviceGroup as type **REG\_SZ**.</span></span> <span data-ttu-id="41d29-115">La entrada de datos para este valor es el nombre del grupo de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="41d29-115">The data entry for this value is the name of the device group.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

<span data-ttu-id="41d29-116">También puede Agregar propiedades de dispositivo personalizadas que no sean iconos, etiqueta y DeviceHandlers en la clave del grupo de dispositivos y, a continuación, aplicarlos a todos los dispositivos que pertenecen a ese grupo de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="41d29-116">You can also add custom device properties other than Icons, Label, and DeviceHandlers under the device group's key and then apply them to all devices that belong to that device group.</span></span>

> [!Note]  
> <span data-ttu-id="41d29-117">Las propiedades que se definen en el nivel de instancia de dispositivo tienen prioridad sobre las propiedades definidas en el nivel de grupo de dispositivos, que a su vez tienen prioridad sobre las propiedades definidas en el nivel de clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d29-117">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



