---
title: Método SetLoadBalancingState de la clase Win32_TSSessionDirectory
description: Establece el valor para indicar si el servidor participará en el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Método SetLoadBalancingState Servicios de Escritorio remoto
- Método SetLoadBalancingState Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685920"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="f1472-106">Método SetLoadBalancingState de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="f1472-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="f1472-107">Establece el valor para indicar si el servidor participará en el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="f1472-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1472-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1472-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="f1472-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1472-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1472-110">*StateValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1472-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1472-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1472-111">Type: **uint32**</span></span>

<span data-ttu-id="f1472-112">Indica si el servidor participará en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f1472-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="f1472-113">0</span><span class="sxs-lookup"><span data-stu-id="f1472-113">0</span></span>
</dt> <dd>

<span data-ttu-id="f1472-114">El servidor no participará en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f1472-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="f1472-115">1</span><span class="sxs-lookup"><span data-stu-id="f1472-115">1</span></span>
</dt> <dd>

<span data-ttu-id="f1472-116">El servidor participará en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f1472-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1472-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1472-117">Remarks</span></span>

<span data-ttu-id="f1472-118">El servidor debe estar unido a una granja de servidores en el agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f1472-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="f1472-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f1472-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f1472-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f1472-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f1472-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f1472-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f1472-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f1472-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1472-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1472-123">Requirements</span></span>



| <span data-ttu-id="f1472-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1472-124">Requirement</span></span> | <span data-ttu-id="f1472-125">Value</span><span class="sxs-lookup"><span data-stu-id="f1472-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1472-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1472-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1472-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f1472-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f1472-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1472-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1472-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1472-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1472-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f1472-130">Namespace</span></span><br/>                | <span data-ttu-id="f1472-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f1472-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f1472-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f1472-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1472-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1472-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1472-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1472-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1472-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1472-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1472-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1472-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1472-137">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="f1472-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

