---
title: Obtener un SDO de máquinas
description: El primer paso en el uso de la API SDO es crear un objeto de equipo SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078003"
---
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="6e3f7-103">Obtener un SDO de máquinas</span><span class="sxs-lookup"><span data-stu-id="6e3f7-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="6e3f7-104">El primer paso en el uso de la API SDO es crear un objeto de equipo SDO.</span><span class="sxs-lookup"><span data-stu-id="6e3f7-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="6e3f7-105">Utilice la función [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para obtener el identificador de clase (CLSID) del objeto de equipo SDO.</span><span class="sxs-lookup"><span data-stu-id="6e3f7-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="6e3f7-106">El identificador de programación (ProgID) que se va a usar para el objeto es "IAS. SdoMachine".</span><span class="sxs-lookup"><span data-stu-id="6e3f7-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="6e3f7-107">Una vez que tenga el CLSID, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con este CLSID.</span><span class="sxs-lookup"><span data-stu-id="6e3f7-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="6e3f7-108">Especifique [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) como la interfaz para la que se va a devolver un puntero.</span><span class="sxs-lookup"><span data-stu-id="6e3f7-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="6e3f7-109">Consulte [adjuntar a un equipo SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver el código de ejemplo que muestra cómo obtener un SDO de máquinas.</span><span class="sxs-lookup"><span data-stu-id="6e3f7-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 