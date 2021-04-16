---
title: Método SetVirtualIPMode de la clase Win32_TSVirtualIP
description: Establece el valor de la propiedad VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Método SetVirtualIPMode Servicios de Escritorio remoto
- Método SetVirtualIPMode Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686053"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="7e954-106">Método SetVirtualIPMode de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="7e954-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="7e954-107">Establece el valor de la propiedad **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="7e954-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e954-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e954-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="7e954-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e954-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e954-110">*VirtualIPMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e954-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e954-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e954-111">Type: **uint32**</span></span>

<span data-ttu-id="7e954-112">Especifica el modo de virtualización de IP que se utiliza en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7e954-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="7e954-113">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e954-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="7e954-114">0</span><span class="sxs-lookup"><span data-stu-id="7e954-114">0</span></span>
</dt> <dd>

<span data-ttu-id="7e954-115">El modo de virtualización de IP es por sesión.</span><span class="sxs-lookup"><span data-stu-id="7e954-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="7e954-116">1</span><span class="sxs-lookup"><span data-stu-id="7e954-116">1</span></span>
</dt> <dd>

<span data-ttu-id="7e954-117">El modo de virtualización de IP es por usuario.</span><span class="sxs-lookup"><span data-stu-id="7e954-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e954-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e954-118">Return value</span></span>

<span data-ttu-id="7e954-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e954-119">Type: **uint32**</span></span>

<span data-ttu-id="7e954-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="7e954-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7e954-121">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7e954-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7e954-122">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="7e954-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e954-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e954-123">Requirements</span></span>



| <span data-ttu-id="7e954-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e954-124">Requirement</span></span> | <span data-ttu-id="7e954-125">Value</span><span class="sxs-lookup"><span data-stu-id="7e954-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e954-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e954-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7e954-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7e954-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7e954-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e954-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7e954-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e954-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="7e954-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e954-130">Namespace</span></span><br/>                | <span data-ttu-id="7e954-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7e954-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7e954-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7e954-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e954-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e954-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e954-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e954-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e954-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e954-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e954-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e954-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e954-137">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="7e954-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





