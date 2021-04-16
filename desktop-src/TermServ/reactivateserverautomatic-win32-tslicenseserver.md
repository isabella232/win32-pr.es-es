---
title: Método ReactivateServerAutomatic de la clase Win32_TSLicenseServer
description: Reactiva el servidor de licencias de Escritorio remoto mediante una conexión automática a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Método ReactivateServerAutomatic Servicios de Escritorio remoto
- Método ReactivateServerAutomatic Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686166"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="444bf-106">Método ReactivateServerAutomatic de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="444bf-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="444bf-107">Reactiva el servidor de licencias de Escritorio remoto mediante una conexión automática a Internet.</span><span class="sxs-lookup"><span data-stu-id="444bf-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="444bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="444bf-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="444bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="444bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="444bf-110">*Motivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="444bf-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="444bf-111">Motivo de la activación.</span><span class="sxs-lookup"><span data-stu-id="444bf-111">Reason for the activation.</span></span> <span data-ttu-id="444bf-112">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="444bf-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="444bf-113">0</span><span class="sxs-lookup"><span data-stu-id="444bf-113">0</span></span>
</dt> <dd>

<span data-ttu-id="444bf-114">Se volvió a implementar el servidor.</span><span class="sxs-lookup"><span data-stu-id="444bf-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="444bf-115">1</span><span class="sxs-lookup"><span data-stu-id="444bf-115">1</span></span>
</dt> <dd>

<span data-ttu-id="444bf-116">El certificado está dañado.</span><span class="sxs-lookup"><span data-stu-id="444bf-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="444bf-117">2</span><span class="sxs-lookup"><span data-stu-id="444bf-117">2</span></span>
</dt> <dd>

<span data-ttu-id="444bf-118">La clave privada se ha puesto en peligro.</span><span class="sxs-lookup"><span data-stu-id="444bf-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="444bf-119">3</span><span class="sxs-lookup"><span data-stu-id="444bf-119">3</span></span>
</dt> <dd>

<span data-ttu-id="444bf-120">Expiró la clave de activación.</span><span class="sxs-lookup"><span data-stu-id="444bf-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="444bf-121">4</span><span class="sxs-lookup"><span data-stu-id="444bf-121">4</span></span>
</dt> <dd>

<span data-ttu-id="444bf-122">El servidor se actualizó.</span><span class="sxs-lookup"><span data-stu-id="444bf-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="444bf-123">*ActivationStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="444bf-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="444bf-124">El estado de activación devuelto puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="444bf-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="444bf-125">0</span><span class="sxs-lookup"><span data-stu-id="444bf-125">0</span></span>
</dt> <dd>

<span data-ttu-id="444bf-126">Se activa el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="444bf-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="444bf-127">1</span><span class="sxs-lookup"><span data-stu-id="444bf-127">1</span></span>
</dt> <dd>

<span data-ttu-id="444bf-128">El servidor de licencias de Escritorio remoto no está activado.</span><span class="sxs-lookup"><span data-stu-id="444bf-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="444bf-129">2</span><span class="sxs-lookup"><span data-stu-id="444bf-129">2</span></span>
</dt> <dd>

<span data-ttu-id="444bf-130">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="444bf-130">An unknown error occurred.</span></span> <span data-ttu-id="444bf-131">No se sabe si el servidor de licencias de Escritorio remoto está activado.</span><span class="sxs-lookup"><span data-stu-id="444bf-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="444bf-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="444bf-132">Return value</span></span>

<span data-ttu-id="444bf-133">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="444bf-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="444bf-134">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="444bf-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="444bf-135">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="444bf-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="444bf-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="444bf-136">Remarks</span></span>

<span data-ttu-id="444bf-137">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="444bf-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="444bf-138">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="444bf-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="444bf-139">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="444bf-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="444bf-140">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="444bf-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="444bf-141">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="444bf-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="444bf-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="444bf-142">Requirements</span></span>



| <span data-ttu-id="444bf-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="444bf-143">Requirement</span></span> | <span data-ttu-id="444bf-144">Value</span><span class="sxs-lookup"><span data-stu-id="444bf-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="444bf-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="444bf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="444bf-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="444bf-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="444bf-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="444bf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="444bf-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="444bf-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="444bf-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="444bf-149">Namespace</span></span><br/>                | <span data-ttu-id="444bf-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="444bf-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="444bf-151">MOF</span><span class="sxs-lookup"><span data-stu-id="444bf-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="444bf-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="444bf-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="444bf-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="444bf-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="444bf-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="444bf-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444bf-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="444bf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444bf-156">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="444bf-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

