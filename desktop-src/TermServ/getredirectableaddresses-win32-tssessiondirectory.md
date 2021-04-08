---
title: Método GetRedirectableAddresses de la clase Win32_TSSessionDirectory
description: Obtiene la lista completa de direcciones DNS válidas.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Método GetRedirectableAddresses Servicios de Escritorio remoto
- Método GetRedirectableAddresses Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078890"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="53a8e-106">Método GetRedirectableAddresses de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="53a8e-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="53a8e-107">Obtiene la lista completa de direcciones DNS válidas.</span><span class="sxs-lookup"><span data-stu-id="53a8e-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a8e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53a8e-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="53a8e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53a8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a8e-110">*fTokenRedirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53a8e-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a8e-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53a8e-111">Type: **uint32**</span></span>

<span data-ttu-id="53a8e-112">Marca que indica si se debe usar el redireccionamiento de tokens.</span><span class="sxs-lookup"><span data-stu-id="53a8e-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="53a8e-113">*IPAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53a8e-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53a8e-114">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="53a8e-114">Type: **string\[\]**</span></span>

<span data-ttu-id="53a8e-115">La lista completa de direcciones IP que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="53a8e-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="53a8e-116">*AdapterNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53a8e-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53a8e-117">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="53a8e-117">Type: **string\[\]**</span></span>

<span data-ttu-id="53a8e-118">La lista de nombres de adaptadores de red que están asociados a las direcciones que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="53a8e-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="53a8e-119">*NetConName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53a8e-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53a8e-120">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="53a8e-120">Type: **string\[\]**</span></span>

<span data-ttu-id="53a8e-121">La lista de nombres de conexión de red que están asociados a las direcciones que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="53a8e-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a8e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53a8e-122">Return value</span></span>

<span data-ttu-id="53a8e-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53a8e-123">Type: **uint32**</span></span>

<span data-ttu-id="53a8e-124">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="53a8e-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="53a8e-125">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="53a8e-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="53a8e-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53a8e-126">Remarks</span></span>

<span data-ttu-id="53a8e-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="53a8e-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="53a8e-128">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="53a8e-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="53a8e-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="53a8e-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="53a8e-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="53a8e-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="53a8e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a8e-131">Requirements</span></span>



| <span data-ttu-id="53a8e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a8e-132">Requirement</span></span> | <span data-ttu-id="53a8e-133">Value</span><span class="sxs-lookup"><span data-stu-id="53a8e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53a8e-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53a8e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="53a8e-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="53a8e-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="53a8e-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53a8e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="53a8e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53a8e-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53a8e-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53a8e-138">Namespace</span></span><br/>                | <span data-ttu-id="53a8e-139">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="53a8e-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="53a8e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="53a8e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53a8e-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53a8e-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="53a8e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53a8e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53a8e-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a8e-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a8e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a8e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a8e-145">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="53a8e-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

