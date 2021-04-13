---
title: Método GetCurrentRedirectableAddresses de la clase Win32_TSSessionDirectory
description: Obtiene la lista configurada actualmente de direcciones válidas DNS que se pueden usar para la redirección.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- Método GetCurrentRedirectableAddresses Servicios de Escritorio remoto
- Método GetCurrentRedirectableAddresses Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método GetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492785"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="22ac3-106">Método GetCurrentRedirectableAddresses de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="22ac3-106">GetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="22ac3-107">Obtiene la lista configurada actualmente de direcciones válidas DNS que se pueden usar para la redirección.</span><span class="sxs-lookup"><span data-stu-id="22ac3-107">Obtains the currently configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ac3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22ac3-108">Syntax</span></span>


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="22ac3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22ac3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ac3-110">*fTokenRedirection* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22ac3-110">*fTokenRedirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22ac3-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22ac3-111">Type: **uint32**</span></span>

<span data-ttu-id="22ac3-112">Marca que indica si se debe usar el redireccionamiento de tokens.</span><span class="sxs-lookup"><span data-stu-id="22ac3-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="22ac3-113">*IPAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22ac3-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22ac3-114">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="22ac3-114">Type: **string\[\]**</span></span>

<span data-ttu-id="22ac3-115">Una matriz de las direcciones IP válidas de DNS configuradas actualmente que se pueden usar para la redirección.</span><span class="sxs-lookup"><span data-stu-id="22ac3-115">An array of the currently configured DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ac3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22ac3-116">Return value</span></span>

<span data-ttu-id="22ac3-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22ac3-117">Type: **uint32**</span></span>

<span data-ttu-id="22ac3-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="22ac3-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="22ac3-119">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="22ac3-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ac3-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22ac3-120">Remarks</span></span>

<span data-ttu-id="22ac3-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="22ac3-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="22ac3-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="22ac3-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="22ac3-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="22ac3-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="22ac3-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="22ac3-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="22ac3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ac3-125">Requirements</span></span>



| <span data-ttu-id="22ac3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ac3-126">Requirement</span></span> | <span data-ttu-id="22ac3-127">Value</span><span class="sxs-lookup"><span data-stu-id="22ac3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22ac3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ac3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22ac3-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="22ac3-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="22ac3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ac3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22ac3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22ac3-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22ac3-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22ac3-132">Namespace</span></span><br/>                | <span data-ttu-id="22ac3-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="22ac3-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="22ac3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="22ac3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22ac3-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22ac3-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="22ac3-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22ac3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ac3-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ac3-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ac3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="22ac3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ac3-139">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="22ac3-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

