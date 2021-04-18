---
title: Método RemoveTSCGroup de la clase Win32_TSLicenseServer
description: RemoveTSCGroup ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Método RemoveTSCGroup Servicios de Escritorio remoto
- Método RemoveTSCGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535380"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5aeb3-106">Método RemoveTSCGroup de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="5aeb3-106">RemoveTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5aeb3-107">\[**RemoveTSCGroup** ya no está disponible para su uso a partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="5aeb3-107">\[**RemoveTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="5aeb3-108">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-108">This method is not supported.</span></span>

<span data-ttu-id="5aeb3-109">**Windows server 2008 R2 y Windows server 2008:** Quita el grupo local de Terminal Server equipos del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-109">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aeb3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aeb3-110">Syntax</span></span>


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="5aeb3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aeb3-111">Parameters</span></span>

<span data-ttu-id="5aeb3-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5aeb3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aeb3-113">Return value</span></span>

<span data-ttu-id="5aeb3-114">Devuelve **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="5aeb3-115">**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5aeb3-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5aeb3-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5aeb3-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5aeb3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aeb3-118">Remarks</span></span>

<span data-ttu-id="5aeb3-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5aeb3-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5aeb3-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5aeb3-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5aeb3-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeb3-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5aeb3-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5aeb3-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aeb3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aeb3-124">Requirements</span></span>



| <span data-ttu-id="5aeb3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aeb3-125">Requirement</span></span> | <span data-ttu-id="5aeb3-126">Value</span><span class="sxs-lookup"><span data-stu-id="5aeb3-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aeb3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aeb3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5aeb3-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5aeb3-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5aeb3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aeb3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5aeb3-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aeb3-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5aeb3-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5aeb3-131">End of client support</span></span><br/>    | <span data-ttu-id="5aeb3-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5aeb3-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5aeb3-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5aeb3-133">End of server support</span></span><br/>    | <span data-ttu-id="5aeb3-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5aeb3-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="5aeb3-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5aeb3-135">Namespace</span></span><br/>                | <span data-ttu-id="5aeb3-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5aeb3-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5aeb3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5aeb3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aeb3-138"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aeb3-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aeb3-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aeb3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aeb3-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aeb3-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aeb3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aeb3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aeb3-142">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="5aeb3-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="5aeb3-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="5aeb3-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

