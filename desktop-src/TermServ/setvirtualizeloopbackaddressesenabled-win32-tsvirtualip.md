---
title: Método SetVirtualizeLoopbackAddressesEnabled de la clase Win32_TSVirtualIP
description: Establece el valor de la propiedad VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Método SetVirtualizeLoopbackAddressesEnabled Servicios de Escritorio remoto
- Método SetVirtualizeLoopbackAddressesEnabled Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676629"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="93e03-106">Método SetVirtualizeLoopbackAddressesEnabled de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="93e03-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="93e03-107">Establece el valor de la propiedad **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="93e03-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e03-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93e03-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="93e03-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93e03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e03-110">*VirtualizeLoopbackAddressesEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93e03-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e03-111">Especifica si se va a habilitar la virtualización de la dirección de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="93e03-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="93e03-112">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="93e03-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="93e03-113">0</span><span class="sxs-lookup"><span data-stu-id="93e03-113">0</span></span>
</dt> <dd>

<span data-ttu-id="93e03-114">No habilite la virtualización de direcciones de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="93e03-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="93e03-115">1</span><span class="sxs-lookup"><span data-stu-id="93e03-115">1</span></span>
</dt> <dd>

<span data-ttu-id="93e03-116">Habilitar la virtualización de direcciones de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="93e03-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e03-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93e03-117">Return value</span></span>

<span data-ttu-id="93e03-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="93e03-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="93e03-119">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="93e03-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="93e03-120">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="93e03-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e03-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e03-121">Requirements</span></span>



| <span data-ttu-id="93e03-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e03-122">Requirement</span></span> | <span data-ttu-id="93e03-123">Value</span><span class="sxs-lookup"><span data-stu-id="93e03-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93e03-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93e03-124">Minimum supported client</span></span><br/> | <span data-ttu-id="93e03-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="93e03-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="93e03-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93e03-126">Minimum supported server</span></span><br/> | <span data-ttu-id="93e03-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93e03-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="93e03-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93e03-128">Namespace</span></span><br/>                | <span data-ttu-id="93e03-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="93e03-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="93e03-130">MOF</span><span class="sxs-lookup"><span data-stu-id="93e03-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93e03-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93e03-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="93e03-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93e03-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e03-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e03-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e03-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="93e03-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e03-135">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="93e03-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





