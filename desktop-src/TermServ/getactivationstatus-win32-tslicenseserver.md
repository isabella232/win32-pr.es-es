---
title: Método GetActivationStatus de la clase Win32_TSLicenseServer
description: Recupera el estado de activación actual del servidor de licencias de Escritorio remoto.
ms.assetid: 1148ffc5-33c1-41f1-b477-78a5293333d1
ms.tgt_platform: multiple
keywords:
- Método GetActivationStatus Servicios de Escritorio remoto
- Método GetActivationStatus Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método GetActivationStatus
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetActivationStatus
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f6209cd13c2372316e6a9606a3bc4fcd60fdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150505"
---
# <a name="getactivationstatus-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5f507-106">Método GetActivationStatus de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="5f507-106">GetActivationStatus method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5f507-107">Recupera el estado de activación actual del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5f507-107">Retrieves the current activation status of the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f507-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f507-108">Syntax</span></span>


```mof
uint32 GetActivationStatus(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5f507-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f507-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f507-110">*ActivationStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5f507-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f507-111">El estado de activación devuelto puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f507-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="5f507-112">0</span><span class="sxs-lookup"><span data-stu-id="5f507-112">0</span></span>
</dt> <dd>

<span data-ttu-id="5f507-113">Se activa el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5f507-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="5f507-114">1</span><span class="sxs-lookup"><span data-stu-id="5f507-114">1</span></span>
</dt> <dd>

<span data-ttu-id="5f507-115">El servidor de licencias de Escritorio remoto no está activado.</span><span class="sxs-lookup"><span data-stu-id="5f507-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="5f507-116">2</span><span class="sxs-lookup"><span data-stu-id="5f507-116">2</span></span>
</dt> <dd>

<span data-ttu-id="5f507-117">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="5f507-117">An unknown error occurred.</span></span> <span data-ttu-id="5f507-118">No se sabe si el servidor de licencias de Escritorio remoto está activado.</span><span class="sxs-lookup"><span data-stu-id="5f507-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f507-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f507-119">Return value</span></span>

<span data-ttu-id="5f507-120">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5f507-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5f507-121">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5f507-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5f507-122">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5f507-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f507-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f507-123">Remarks</span></span>

<span data-ttu-id="5f507-124">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="5f507-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5f507-125">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5f507-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5f507-126">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5f507-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5f507-127">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5f507-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5f507-128">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5f507-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f507-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f507-129">Requirements</span></span>



| <span data-ttu-id="5f507-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f507-130">Requirement</span></span> | <span data-ttu-id="5f507-131">Value</span><span class="sxs-lookup"><span data-stu-id="5f507-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f507-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f507-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5f507-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f507-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5f507-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f507-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5f507-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f507-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5f507-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f507-136">Namespace</span></span><br/>                | <span data-ttu-id="5f507-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5f507-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5f507-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5f507-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f507-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f507-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f507-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f507-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f507-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f507-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f507-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f507-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f507-143">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="5f507-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

