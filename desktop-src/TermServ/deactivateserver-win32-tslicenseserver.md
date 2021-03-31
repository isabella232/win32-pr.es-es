---
title: Método DeactivateServer de la clase Win32_TSLicenseServer
description: Desactiva el servidor de licencias de Escritorio remoto mediante un código de confirmación que se recibe a través del teléfono.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- Método DeactivateServer Servicios de Escritorio remoto
- Método DeactivateServer Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método DeactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996023"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="eb4b6-106">Método DeactivateServer de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="eb4b6-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="eb4b6-107">Desactiva el servidor de licencias de Escritorio remoto mediante un código de confirmación que se recibe a través del teléfono.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4b6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb4b6-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="eb4b6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb4b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4b6-110">*sConfirmCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eb4b6-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4b6-111">Código de confirmación.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="eb4b6-112">*ActivationStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eb4b6-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4b6-113">El estado de activación devuelto puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="eb4b6-114">0</span><span class="sxs-lookup"><span data-stu-id="eb4b6-114">0</span></span>
</dt> <dd>

<span data-ttu-id="eb4b6-115">Se activa el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="eb4b6-116">1</span><span class="sxs-lookup"><span data-stu-id="eb4b6-116">1</span></span>
</dt> <dd>

<span data-ttu-id="eb4b6-117">El servidor de licencias de Escritorio remoto no está activado.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="eb4b6-118">2</span><span class="sxs-lookup"><span data-stu-id="eb4b6-118">2</span></span>
</dt> <dd>

<span data-ttu-id="eb4b6-119">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-119">An unknown error occurred.</span></span> <span data-ttu-id="eb4b6-120">No se sabe si el servidor de licencias de Servicios de Escritorio remoto está activado.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4b6-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb4b6-121">Return value</span></span>

<span data-ttu-id="eb4b6-122">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eb4b6-123">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eb4b6-124">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="eb4b6-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4b6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb4b6-125">Remarks</span></span>

<span data-ttu-id="eb4b6-126">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eb4b6-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eb4b6-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eb4b6-128">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eb4b6-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="eb4b6-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eb4b6-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eb4b6-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4b6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb4b6-131">Requirements</span></span>



| <span data-ttu-id="eb4b6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb4b6-132">Requirement</span></span> | <span data-ttu-id="eb4b6-133">Value</span><span class="sxs-lookup"><span data-stu-id="eb4b6-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4b6-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb4b6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4b6-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eb4b6-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="eb4b6-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb4b6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4b6-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb4b6-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="eb4b6-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb4b6-138">Namespace</span></span><br/>                | <span data-ttu-id="eb4b6-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="eb4b6-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="eb4b6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="eb4b6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb4b6-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb4b6-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb4b6-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb4b6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb4b6-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb4b6-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4b6-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb4b6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4b6-145">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="eb4b6-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

