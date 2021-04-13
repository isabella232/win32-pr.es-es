---
title: Método SetCurrentRedirectableAddresses de la clase Win32_TSSessionDirectory
description: Establece la lista configurada de direcciones DNS válidas que se pueden usar para la redirección.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Método SetCurrentRedirectableAddresses Servicios de Escritorio remoto
- Método SetCurrentRedirectableAddresses Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422468"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="c7152-106">Método SetCurrentRedirectableAddresses de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="c7152-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="c7152-107">El método **SetCurrentRedirectableAddresses** establece la lista configurada de direcciones DNS válidas que se pueden usar para la redirección.</span><span class="sxs-lookup"><span data-stu-id="c7152-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7152-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7152-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="c7152-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7152-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7152-110">*fTokenRedirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7152-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7152-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7152-111">Type: **uint32**</span></span>

<span data-ttu-id="c7152-112">Marca que indica si se debe usar el redireccionamiento de tokens.</span><span class="sxs-lookup"><span data-stu-id="c7152-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="c7152-113">*IPAddresses* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7152-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7152-114">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c7152-114">Type: **string\[\]**</span></span>

<span data-ttu-id="c7152-115">Matriz de cadenas que representa la lista de direcciones IP válidas DNS que se pueden usar para la redirección.</span><span class="sxs-lookup"><span data-stu-id="c7152-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7152-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7152-116">Return value</span></span>

<span data-ttu-id="c7152-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7152-117">Type: **uint32**</span></span>

<span data-ttu-id="c7152-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="c7152-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="c7152-119">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c7152-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7152-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7152-120">Remarks</span></span>

<span data-ttu-id="c7152-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c7152-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c7152-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c7152-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c7152-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c7152-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c7152-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c7152-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7152-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7152-125">Requirements</span></span>



| <span data-ttu-id="c7152-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7152-126">Requirement</span></span> | <span data-ttu-id="c7152-127">Value</span><span class="sxs-lookup"><span data-stu-id="c7152-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7152-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7152-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c7152-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c7152-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7152-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7152-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c7152-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7152-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7152-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7152-132">Namespace</span></span><br/>                | <span data-ttu-id="c7152-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c7152-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c7152-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c7152-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7152-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7152-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7152-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7152-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7152-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7152-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7152-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7152-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7152-139">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="c7152-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

