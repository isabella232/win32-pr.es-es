---
title: Método SetNetworkAdapterLanaID de la clase Win32_TSNetworkAdapterSetting
description: Especifica el número de adaptador de red de área local (LANA) del adaptador de red que se va a establecer.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Método SetNetworkAdapterLanaID Servicios de Escritorio remoto
- Método SetNetworkAdapterLanaID Servicios de Escritorio remoto, clase Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de clase Servicios de Escritorio remoto, método SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803770"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="a4a32-106">Método SetNetworkAdapterLanaID de la \_ clase TSNetworkAdapterSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="a4a32-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="a4a32-107">El método **SetNetworkAdapterLanaID** especifica el número de adaptador de red de área local (lana) del adaptador de red que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a4a32-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="a4a32-108">Si el ID. de LANA especificado no es válido o no existe, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a4a32-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="a4a32-109">La lista de identificadores de LANA disponible se obtiene enumerando la propiedad **DeviceIDList** en la clase [**\_ TSNetworkAdapterSetting de Win32**](win32-tsnetworkadaptersetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a32-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a32-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4a32-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="a4a32-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4a32-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a32-112">*NetworkAdapterLanaID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4a32-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a32-113">Número LANA del adaptador de red que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a4a32-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a32-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4a32-114">Return value</span></span>

<span data-ttu-id="a4a32-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="a4a32-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a4a32-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a4a32-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a32-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4a32-117">Remarks</span></span>

<span data-ttu-id="a4a32-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4a32-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4a32-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a4a32-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a4a32-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a32-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4a32-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4a32-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a32-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a32-122">Requirements</span></span>



| <span data-ttu-id="a4a32-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a32-123">Requirement</span></span> | <span data-ttu-id="a4a32-124">Value</span><span class="sxs-lookup"><span data-stu-id="a4a32-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a32-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4a32-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a32-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4a32-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4a32-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4a32-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a32-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4a32-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4a32-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a4a32-129">Namespace</span></span><br/>                | <span data-ttu-id="a4a32-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a4a32-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a4a32-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a4a32-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4a32-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4a32-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4a32-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4a32-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a32-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4a32-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a32-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4a32-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a32-136">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="a4a32-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

