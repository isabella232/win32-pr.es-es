---
title: Método SelectAllNetworkAdapters de la clase Win32_TSNetworkAdapterSetting
description: El método SelectAllNetworkAdapters selecciona todos los adaptadores de red.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Método SelectAllNetworkAdapters Servicios de Escritorio remoto
- Método SelectAllNetworkAdapters Servicios de Escritorio remoto, clase Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de clase Servicios de Escritorio remoto, método SelectAllNetworkAdapters
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359771"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="a9ce9-106">Método SelectAllNetworkAdapters de la \_ clase TSNetworkAdapterSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="a9ce9-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="a9ce9-107">El método **SelectAllNetworkAdapters** selecciona todos los adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="a9ce9-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ce9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9ce9-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="a9ce9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9ce9-109">Parameters</span></span>

<span data-ttu-id="a9ce9-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a9ce9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9ce9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9ce9-111">Return value</span></span>

<span data-ttu-id="a9ce9-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="a9ce9-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a9ce9-113">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a9ce9-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9ce9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9ce9-114">Remarks</span></span>

<span data-ttu-id="a9ce9-115">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a9ce9-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a9ce9-116">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a9ce9-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a9ce9-117">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a9ce9-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a9ce9-118">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a9ce9-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ce9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ce9-119">Requirements</span></span>



| <span data-ttu-id="a9ce9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ce9-120">Requirement</span></span> | <span data-ttu-id="a9ce9-121">Value</span><span class="sxs-lookup"><span data-stu-id="a9ce9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ce9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9ce9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ce9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9ce9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9ce9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9ce9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ce9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9ce9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9ce9-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9ce9-126">Namespace</span></span><br/>                | <span data-ttu-id="a9ce9-127">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a9ce9-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a9ce9-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ce9-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ce9-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ce9-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ce9-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9ce9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ce9-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ce9-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ce9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9ce9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ce9-133">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="a9ce9-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

