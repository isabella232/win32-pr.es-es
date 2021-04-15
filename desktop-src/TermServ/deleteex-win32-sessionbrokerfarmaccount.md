---
title: Método DeleteEx de la clase Win32_SessionBrokerFarmAccount
description: La \_ clase Win32 SessionBrokerFarmAccount ya no está disponible para su uso a partir de Windows Server 2012. | Método DeleteEx de la clase Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Método DeleteEx Servicios de Escritorio remoto
- Método DeleteEx Servicios de Escritorio remoto, clase Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount de clase Servicios de Escritorio remoto, método DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689715"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="1ec51-107">Método DeleteEx de la \_ clase SessionBrokerFarmAccount de Win32</span><span class="sxs-lookup"><span data-stu-id="1ec51-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="1ec51-108">\[La clase [**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) ya no está disponible para su uso a partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="1ec51-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="1ec51-109">Elimina la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="1ec51-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec51-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ec51-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="1ec51-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ec51-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec51-112">*DeleteComputerObject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ec51-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec51-113">Indica si el objeto de equipo asociado a la granja se va a quitar de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ec51-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec51-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ec51-114">Return value</span></span>

<span data-ttu-id="1ec51-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="1ec51-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1ec51-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1ec51-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec51-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec51-117">Requirements</span></span>



| <span data-ttu-id="1ec51-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec51-118">Requirement</span></span> | <span data-ttu-id="1ec51-119">Value</span><span class="sxs-lookup"><span data-stu-id="1ec51-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec51-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ec51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec51-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1ec51-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1ec51-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ec51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec51-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ec51-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="1ec51-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1ec51-124">End of client support</span></span><br/>    | <span data-ttu-id="1ec51-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1ec51-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1ec51-126">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1ec51-126">End of server support</span></span><br/>    | <span data-ttu-id="1ec51-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ec51-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="1ec51-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1ec51-128">Namespace</span></span><br/>                | <span data-ttu-id="1ec51-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1ec51-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="1ec51-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1ec51-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ec51-131"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ec51-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ec51-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ec51-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ec51-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec51-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec51-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ec51-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec51-135">**Win32 \_ SessionBrokerFarmAccount**</span><span class="sxs-lookup"><span data-stu-id="1ec51-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





