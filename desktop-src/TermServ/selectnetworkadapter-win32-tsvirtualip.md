---
title: Método SelectNetworkAdapter de la clase Win32_TSVirtualIP
description: Establece la dirección MAC del adaptador de red que se va a usar para la virtualización de IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Método SelectNetworkAdapter Servicios de Escritorio remoto
- Método SelectNetworkAdapter Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996310"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="0d981-106">Método SelectNetworkAdapter de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="0d981-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="0d981-107">Establece la dirección MAC del adaptador de red que se va a usar para la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="0d981-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d981-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d981-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="0d981-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d981-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d981-110">*NetworkAdapterMacAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d981-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d981-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="0d981-111">Type: **string**</span></span>

<span data-ttu-id="0d981-112">Especifica la dirección MAC del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="0d981-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d981-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d981-113">Return value</span></span>

<span data-ttu-id="0d981-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d981-114">Type: **uint32**</span></span>

<span data-ttu-id="0d981-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="0d981-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0d981-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0d981-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="0d981-117">Si la dirección MAC no es válida o no existe, o si el modo de virtualización de IP es por sesión, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="0d981-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="0d981-118">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d981-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d981-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d981-119">Requirements</span></span>



| <span data-ttu-id="0d981-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d981-120">Requirement</span></span> | <span data-ttu-id="0d981-121">Value</span><span class="sxs-lookup"><span data-stu-id="0d981-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d981-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d981-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d981-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0d981-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0d981-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d981-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d981-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d981-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="0d981-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d981-126">Namespace</span></span><br/>                | <span data-ttu-id="0d981-127">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0d981-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0d981-128">MOF</span><span class="sxs-lookup"><span data-stu-id="0d981-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d981-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d981-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d981-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d981-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d981-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d981-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d981-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d981-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d981-133">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="0d981-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





