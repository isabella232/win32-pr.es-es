---
title: Método ReactivateServer de la clase Win32_TSLicenseServer
description: Reactiva el servidor de licencias de Escritorio remoto mediante un nuevo identificador que se obtuvo a través del teléfono o Internet.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- Método ReactivateServer Servicios de Escritorio remoto
- Método ReactivateServer Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ReactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e84eb0bed0b52ad463fce50ce334d6c8eb8d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490601"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5301a-106">Método ReactivateServer de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="5301a-106">ReactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5301a-107">Reactiva el servidor de licencias de Escritorio remoto mediante un nuevo identificador que se obtuvo a través del teléfono o Internet.</span><span class="sxs-lookup"><span data-stu-id="5301a-107">Reactivates the Remote Desktop license server by using a new identifier that was obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="5301a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5301a-108">Syntax</span></span>


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5301a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5301a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5301a-110">*sNewLicenseServerId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5301a-110">*sNewLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5301a-111">Escritorio remoto identificador del servidor de licencias que se obtuvo a través del teléfono o Internet.</span><span class="sxs-lookup"><span data-stu-id="5301a-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="5301a-112">*ActivationStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5301a-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5301a-113">El estado de activación devuelto puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5301a-113">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="5301a-114">0</span><span class="sxs-lookup"><span data-stu-id="5301a-114">0</span></span>
</dt> <dd>

<span data-ttu-id="5301a-115">Se activa el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5301a-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="5301a-116">1</span><span class="sxs-lookup"><span data-stu-id="5301a-116">1</span></span>
</dt> <dd>

<span data-ttu-id="5301a-117">El servidor de licencias de Escritorio remoto no está activado.</span><span class="sxs-lookup"><span data-stu-id="5301a-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="5301a-118">2</span><span class="sxs-lookup"><span data-stu-id="5301a-118">2</span></span>
</dt> <dd>

<span data-ttu-id="5301a-119">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="5301a-119">An unknown error occurred.</span></span> <span data-ttu-id="5301a-120">No se sabe si el servidor de licencias de Escritorio remoto está activado.</span><span class="sxs-lookup"><span data-stu-id="5301a-120">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5301a-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5301a-121">Return value</span></span>

<span data-ttu-id="5301a-122">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5301a-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5301a-123">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5301a-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5301a-124">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5301a-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5301a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5301a-125">Remarks</span></span>

<span data-ttu-id="5301a-126">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="5301a-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5301a-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5301a-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5301a-128">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5301a-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5301a-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5301a-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5301a-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5301a-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5301a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5301a-131">Requirements</span></span>



| <span data-ttu-id="5301a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5301a-132">Requirement</span></span> | <span data-ttu-id="5301a-133">Value</span><span class="sxs-lookup"><span data-stu-id="5301a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5301a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5301a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5301a-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5301a-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5301a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5301a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5301a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5301a-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5301a-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5301a-138">Namespace</span></span><br/>                | <span data-ttu-id="5301a-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5301a-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5301a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5301a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5301a-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5301a-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5301a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5301a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5301a-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5301a-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5301a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5301a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5301a-145">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="5301a-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

