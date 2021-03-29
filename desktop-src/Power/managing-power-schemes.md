---
description: Administración de combinaciones de energía
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Administración de combinaciones de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667210"
---
# <a name="power-scheme-management"></a><span data-ttu-id="fc477-103">Administración de combinaciones de energía</span><span class="sxs-lookup"><span data-stu-id="fc477-103">Power Scheme Management</span></span>

<span data-ttu-id="fc477-104">Cada plan de energía se identifica de forma única mediante un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="fc477-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="fc477-105">Para enumerar todos los esquemas de energía disponibles, utilice la función [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) .</span><span class="sxs-lookup"><span data-stu-id="fc477-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="fc477-106">**PowerEnumerate** también se puede usar para recuperar toda la configuración de energía de un esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="fc477-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="fc477-107">El plan de energía que se usa actualmente en el sistema se conoce como plan de energía activo o plan.</span><span class="sxs-lookup"><span data-stu-id="fc477-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="fc477-108">Para recuperar el **GUID** del plan activo, llame a la función [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="fc477-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="fc477-109">Para cambiar el plan de energía activo, llame a la función [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="fc477-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="fc477-110">Para crear un plan de energía, primero debe duplicar un esquema existente mediante la función [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , especificando el **GUID** del esquema en el que desea basar el nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="fc477-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="fc477-111">Debe copiar uno de los esquemas integrados y modificar la configuración de energía según sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="fc477-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="fc477-112">Tenga en cuenta que al crear un plan de energía, no se actualiza automáticamente el plan de energía activo.</span><span class="sxs-lookup"><span data-stu-id="fc477-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="fc477-113">Siempre debe llamar a [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) para actualizar el plan de energía activo.</span><span class="sxs-lookup"><span data-stu-id="fc477-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="fc477-114">Los planes de energía existentes se pueden modificar y aplicar de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="fc477-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="fc477-115">Para quitar un plan de energía, llame a la función [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .</span><span class="sxs-lookup"><span data-stu-id="fc477-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="fc477-116">Para recuperar información adicional sobre el estado de energía del sistema, llame a la función [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .</span><span class="sxs-lookup"><span data-stu-id="fc477-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fc477-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc477-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc477-118">Planes de energía</span><span class="sxs-lookup"><span data-stu-id="fc477-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



