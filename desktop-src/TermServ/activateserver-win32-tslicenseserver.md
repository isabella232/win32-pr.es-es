---
title: Método ActivateServer de la clase Win32_TSLicenseServer
description: Activa el servidor de licencias de Escritorio remoto mediante un identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Método ActivateServer Servicios de Escritorio remoto
- Método ActivateServer Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ActivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686184"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a2311-106">Método ActivateServer de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="a2311-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a2311-107">Activa el servidor de licencias de Escritorio remoto mediante un identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.</span><span class="sxs-lookup"><span data-stu-id="a2311-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2311-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2311-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a2311-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2311-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2311-110">*sLicenseServerId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2311-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2311-111">Escritorio remoto identificador del servidor de licencias que se obtuvo a través del teléfono o Internet.</span><span class="sxs-lookup"><span data-stu-id="a2311-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="a2311-112">El parámetro *sLicenseServerId* es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.</span><span class="sxs-lookup"><span data-stu-id="a2311-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="a2311-113">*ActivationStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a2311-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2311-114">El estado de activación devuelto puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a2311-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="a2311-115">0</span><span class="sxs-lookup"><span data-stu-id="a2311-115">0</span></span>
</dt> <dd>

<span data-ttu-id="a2311-116">Se activa el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a2311-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="a2311-117">1</span><span class="sxs-lookup"><span data-stu-id="a2311-117">1</span></span>
</dt> <dd>

<span data-ttu-id="a2311-118">El servidor de licencias de Escritorio remoto no está activado.</span><span class="sxs-lookup"><span data-stu-id="a2311-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="a2311-119">2</span><span class="sxs-lookup"><span data-stu-id="a2311-119">2</span></span>
</dt> <dd>

<span data-ttu-id="a2311-120">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="a2311-120">An unknown error occurred.</span></span> <span data-ttu-id="a2311-121">No se sabe si el servidor de licencias de Escritorio remoto está activado.</span><span class="sxs-lookup"><span data-stu-id="a2311-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2311-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2311-122">Return value</span></span>

<span data-ttu-id="a2311-123">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a2311-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a2311-124">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a2311-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a2311-125">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a2311-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2311-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2311-126">Remarks</span></span>

<span data-ttu-id="a2311-127">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="a2311-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a2311-128">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a2311-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a2311-129">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a2311-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a2311-130">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a2311-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a2311-131">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a2311-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2311-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2311-132">Requirements</span></span>



| <span data-ttu-id="a2311-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2311-133">Requirement</span></span> | <span data-ttu-id="a2311-134">Value</span><span class="sxs-lookup"><span data-stu-id="a2311-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2311-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2311-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a2311-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a2311-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a2311-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2311-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a2311-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2311-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a2311-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2311-139">Namespace</span></span><br/>                | <span data-ttu-id="a2311-140">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a2311-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a2311-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a2311-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2311-142"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2311-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2311-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2311-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2311-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2311-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2311-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2311-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2311-146">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="a2311-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

