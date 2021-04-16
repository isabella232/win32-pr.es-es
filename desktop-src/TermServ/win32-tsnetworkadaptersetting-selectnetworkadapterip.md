---
title: Método SelectNetworkAdapterIP de la clase Win32_TSNetworkAdapterSetting
description: Selecciona un adaptador de red basado en la dirección IP del adaptador.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Método SelectNetworkAdapterIP Servicios de Escritorio remoto
- Método SelectNetworkAdapterIP Servicios de Escritorio remoto, clase Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de clase Servicios de Escritorio remoto, método SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685955"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="e7d88-106">Método SelectNetworkAdapterIP de la \_ clase TSNetworkAdapterSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="e7d88-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="e7d88-107">Selecciona un adaptador de red basado en la dirección IP del adaptador.</span><span class="sxs-lookup"><span data-stu-id="e7d88-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d88-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7d88-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="e7d88-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7d88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d88-110">*NetworkAdapterIP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7d88-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d88-111">Dirección IP del adaptador de red que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="e7d88-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d88-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7d88-112">Return value</span></span>

<span data-ttu-id="e7d88-113">Devuelve cero si la dirección IP especificada es válida y devuelve un código de error de WMI si la dirección IP no es válida o no existe.</span><span class="sxs-lookup"><span data-stu-id="e7d88-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="e7d88-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e7d88-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d88-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7d88-115">Remarks</span></span>

<span data-ttu-id="e7d88-116">Puede recuperar la dirección IP de un adaptador de red mediante la enumeración de las propiedades de la clase [**\_ TSNetworkAdapterListSetting de Win32**](win32-tsnetworkadapterlistsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d88-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="e7d88-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e7d88-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e7d88-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e7d88-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e7d88-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e7d88-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e7d88-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e7d88-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d88-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7d88-121">Requirements</span></span>



| <span data-ttu-id="e7d88-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7d88-122">Requirement</span></span> | <span data-ttu-id="e7d88-123">Value</span><span class="sxs-lookup"><span data-stu-id="e7d88-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d88-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7d88-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d88-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7d88-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7d88-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7d88-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d88-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7d88-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7d88-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7d88-128">Namespace</span></span><br/>                | <span data-ttu-id="e7d88-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e7d88-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e7d88-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e7d88-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7d88-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7d88-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7d88-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7d88-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7d88-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7d88-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d88-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7d88-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d88-135">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="e7d88-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

