---
description: Representa un dispositivo de teclado sintético.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652377"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="b27a7-103">MSVM \_ SyntheticKeyboard (clase)</span><span class="sxs-lookup"><span data-stu-id="b27a7-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="b27a7-104">Representa un dispositivo de teclado sintético.</span><span class="sxs-lookup"><span data-stu-id="b27a7-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="b27a7-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b27a7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27a7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b27a7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="b27a7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b27a7-107">Members</span></span>

<span data-ttu-id="b27a7-108">La clase **MSVM \_ SyntheticKeyboard** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b27a7-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="b27a7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b27a7-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b27a7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b27a7-110">Methods</span></span>

<span data-ttu-id="b27a7-111">La clase **MSVM \_ SyntheticKeyboard** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b27a7-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="b27a7-112">Método</span><span class="sxs-lookup"><span data-stu-id="b27a7-112">Method</span></span>                                                                  | <span data-ttu-id="b27a7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b27a7-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="b27a7-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b27a7-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="b27a7-115">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="b27a7-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="b27a7-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b27a7-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="b27a7-117">restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b27a7-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="b27a7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b27a7-118">Requirements</span></span>



| <span data-ttu-id="b27a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b27a7-119">Requirement</span></span> | <span data-ttu-id="b27a7-120">Value</span><span class="sxs-lookup"><span data-stu-id="b27a7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27a7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b27a7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b27a7-122">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b27a7-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b27a7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b27a7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b27a7-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b27a7-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b27a7-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b27a7-125">Namespace</span></span><br/>                | <span data-ttu-id="b27a7-126">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b27a7-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b27a7-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b27a7-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b27a7-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b27a7-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b27a7-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b27a7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b27a7-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b27a7-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b27a7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b27a7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27a7-132">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b27a7-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




