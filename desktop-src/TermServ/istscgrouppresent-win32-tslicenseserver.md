---
title: Método IsTSCGroupPresent de la clase Win32_TSLicenseServer
description: IsTSCGroupPresent ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Método IsTSCGroupPresent Servicios de Escritorio remoto
- Método IsTSCGroupPresent Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079149"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="d9de3-106">Método IsTSCGroupPresent de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="d9de3-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="d9de3-107">\[**IsTSCGroupPresent** ya no está disponible para su uso a partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="d9de3-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="d9de3-108">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="d9de3-108">This method is not supported.</span></span>

<span data-ttu-id="d9de3-109">**Windows server 2008 R2 y Windows server 2008:** Recupera si el grupo local de equipos Terminal Server existe en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d9de3-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9de3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9de3-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="d9de3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9de3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9de3-112">*Presente* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d9de3-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9de3-113">Valor booleano que indica si existe el grupo local de equipos Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d9de3-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9de3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9de3-114">Return value</span></span>

<span data-ttu-id="d9de3-115">Devuelve **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="d9de3-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="d9de3-116">**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d9de3-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d9de3-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d9de3-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d9de3-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d9de3-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9de3-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9de3-119">Remarks</span></span>

<span data-ttu-id="d9de3-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d9de3-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d9de3-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d9de3-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d9de3-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d9de3-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d9de3-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d9de3-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d9de3-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d9de3-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9de3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9de3-125">Requirements</span></span>



| <span data-ttu-id="d9de3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9de3-126">Requirement</span></span> | <span data-ttu-id="d9de3-127">Value</span><span class="sxs-lookup"><span data-stu-id="d9de3-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9de3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9de3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d9de3-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d9de3-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d9de3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9de3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d9de3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9de3-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d9de3-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d9de3-132">End of client support</span></span><br/>    | <span data-ttu-id="d9de3-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d9de3-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d9de3-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d9de3-134">End of server support</span></span><br/>    | <span data-ttu-id="d9de3-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9de3-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="d9de3-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9de3-136">Namespace</span></span><br/>                | <span data-ttu-id="d9de3-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d9de3-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d9de3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d9de3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9de3-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9de3-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9de3-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9de3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9de3-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9de3-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9de3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9de3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9de3-143">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="d9de3-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

