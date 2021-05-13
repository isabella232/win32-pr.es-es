---
description: Colección de objetos DeviceInfo que representa todos los dispositivos instalados en el equipo.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Wia.Devices, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841317"
---
# <a name="wiadevices-property"></a><span data-ttu-id="24331-103">Wia.Devices, propiedad</span><span class="sxs-lookup"><span data-stu-id="24331-103">Wia.Devices property</span></span>

<span data-ttu-id="24331-104">Colección de [**objetos DeviceInfo**](-wia-deviceinfo.md) que representa todos los dispositivos instalados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="24331-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="24331-105">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="24331-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="24331-106">Esta colección está basada en 0.</span><span class="sxs-lookup"><span data-stu-id="24331-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="24331-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="24331-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24331-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24331-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="24331-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="24331-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="24331-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="24331-110">Examples</span></span>

<span data-ttu-id="24331-111">En el ejemplo siguiente se muestra el uso de la **colección Devices** para enumerar los dispositivos de un sistema.</span><span class="sxs-lookup"><span data-stu-id="24331-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="24331-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24331-112">Requirements</span></span>



| <span data-ttu-id="24331-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="24331-113">Requirement</span></span> | <span data-ttu-id="24331-114">Value</span><span class="sxs-lookup"><span data-stu-id="24331-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24331-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24331-115">Minimum supported client</span></span><br/> | <span data-ttu-id="24331-116">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="24331-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24331-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24331-117">Minimum supported server</span></span><br/> | <span data-ttu-id="24331-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="24331-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="24331-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24331-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24331-120"><dt>Wiascr.dll (versión 4.90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="24331-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




