---
title: Método SetVirtualIPActive de la clase Win32_TSVirtualIP
description: Establece el valor de la propiedad VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Método SetVirtualIPActive Servicios de Escritorio remoto
- Método SetVirtualIPActive Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996588"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="08480-106">Método SetVirtualIPActive de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="08480-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="08480-107">Establece el valor de la propiedad **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="08480-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="08480-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08480-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="08480-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08480-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08480-110">*VirtualIPActive* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08480-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08480-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08480-111">Type: **uint32**</span></span>

<span data-ttu-id="08480-112">Especifica si la virtualización de IP está activa en el servidor.</span><span class="sxs-lookup"><span data-stu-id="08480-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="08480-113">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="08480-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="08480-114">cero</span><span class="sxs-lookup"><span data-stu-id="08480-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="08480-115">La virtualización de IP no está activa.</span><span class="sxs-lookup"><span data-stu-id="08480-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="08480-116">distinto</span><span class="sxs-lookup"><span data-stu-id="08480-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="08480-117">La virtualización de IP está activa.</span><span class="sxs-lookup"><span data-stu-id="08480-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08480-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08480-118">Return value</span></span>

<span data-ttu-id="08480-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08480-119">Type: **uint32**</span></span>

<span data-ttu-id="08480-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="08480-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="08480-121">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="08480-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="08480-122">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="08480-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="08480-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08480-123">Requirements</span></span>



| <span data-ttu-id="08480-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08480-124">Requirement</span></span> | <span data-ttu-id="08480-125">Value</span><span class="sxs-lookup"><span data-stu-id="08480-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08480-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08480-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08480-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="08480-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="08480-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08480-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08480-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08480-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="08480-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08480-130">Namespace</span></span><br/>                | <span data-ttu-id="08480-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="08480-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="08480-132">MOF</span><span class="sxs-lookup"><span data-stu-id="08480-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08480-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08480-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="08480-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08480-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08480-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08480-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08480-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="08480-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08480-137">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="08480-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





