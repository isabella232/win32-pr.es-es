---
title: Método CreateTSCGroup de la clase Win32_TSLicenseServer
description: CreateTSCGroup ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Método CreateTSCGroup Servicios de Escritorio remoto
- Método CreateTSCGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método CreateTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905070"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="9e734-106">Método CreateTSCGroup de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="9e734-106">CreateTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="9e734-107">\[**CreateTSCGroup** ya no está disponible para su uso a partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="9e734-107">\[**CreateTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="9e734-108">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9e734-108">This method is not supported.</span></span>

<span data-ttu-id="9e734-109">**Windows server 2008 R2 y Windows server 2008:** Crea el grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9e734-109">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e734-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e734-110">Syntax</span></span>


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="9e734-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e734-111">Parameters</span></span>

<span data-ttu-id="9e734-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9e734-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e734-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e734-113">Return value</span></span>

<span data-ttu-id="9e734-114">Devuelve **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="9e734-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="9e734-115">**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9e734-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9e734-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9e734-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9e734-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9e734-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e734-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e734-118">Remarks</span></span>

<span data-ttu-id="9e734-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="9e734-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9e734-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9e734-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9e734-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9e734-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9e734-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="9e734-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9e734-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9e734-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e734-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e734-124">Requirements</span></span>



| <span data-ttu-id="9e734-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e734-125">Requirement</span></span> | <span data-ttu-id="9e734-126">Value</span><span class="sxs-lookup"><span data-stu-id="9e734-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e734-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e734-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9e734-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9e734-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9e734-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e734-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9e734-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e734-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9e734-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9e734-131">End of client support</span></span><br/>    | <span data-ttu-id="9e734-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9e734-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9e734-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9e734-133">End of server support</span></span><br/>    | <span data-ttu-id="9e734-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e734-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="9e734-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9e734-135">Namespace</span></span><br/>                | <span data-ttu-id="9e734-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9e734-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9e734-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9e734-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e734-138"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e734-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e734-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e734-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e734-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e734-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e734-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e734-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e734-142">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="9e734-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="9e734-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="9e734-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

