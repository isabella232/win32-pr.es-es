---
title: Método ChangeRole de la clase Win32_TSLicenseServer
description: Cambia el ámbito de detección del servidor de licencias de Escritorio remoto. El ámbito de detección determina qué servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) de la red pueden detectar automáticamente el servidor de licencias.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Método ChangeRole Servicios de Escritorio remoto
- Método ChangeRole Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489688"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="ef707-107">Método ChangeRole de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="ef707-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="ef707-108">Cambia el ámbito de detección del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ef707-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="ef707-109">El ámbito de detección determina qué servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) de la red pueden detectar automáticamente el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef707-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef707-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef707-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="ef707-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef707-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef707-112">Función de la  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef707-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef707-113">Ámbito de detección del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ef707-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="ef707-114">Puede establecer uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ef707-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="ef707-115">0</span><span class="sxs-lookup"><span data-stu-id="ef707-115">0</span></span>
</dt> <dd>

<span data-ttu-id="ef707-116">Los servidores host de sesión de escritorio remoto del mismo grupo de trabajo pueden detectar el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef707-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="ef707-117">1</span><span class="sxs-lookup"><span data-stu-id="ef707-117">1</span></span>
</dt> <dd>

<span data-ttu-id="ef707-118">Los servidores host de sesión de escritorio remoto del mismo dominio pueden detectar el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef707-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="ef707-119">Debe haber iniciado sesión como administrador de dominio para establecer este valor.</span><span class="sxs-lookup"><span data-stu-id="ef707-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="ef707-120">2</span><span class="sxs-lookup"><span data-stu-id="ef707-120">2</span></span>
</dt> <dd>

<span data-ttu-id="ef707-121">Los servidores host de sesión de escritorio remoto de varios dominios del mismo bosque pueden detectar el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef707-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="ef707-122">Debe haber iniciado sesión como administrador de empresa para establecer este valor.</span><span class="sxs-lookup"><span data-stu-id="ef707-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef707-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef707-123">Return value</span></span>

<span data-ttu-id="ef707-124">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="ef707-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ef707-125">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ef707-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ef707-126">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ef707-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef707-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef707-127">Remarks</span></span>

<span data-ttu-id="ef707-128">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="ef707-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ef707-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ef707-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ef707-130">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ef707-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ef707-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ef707-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ef707-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ef707-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef707-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef707-133">Requirements</span></span>



| <span data-ttu-id="ef707-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef707-134">Requirement</span></span> | <span data-ttu-id="ef707-135">Value</span><span class="sxs-lookup"><span data-stu-id="ef707-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef707-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef707-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ef707-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ef707-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ef707-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef707-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ef707-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef707-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ef707-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef707-140">Namespace</span></span><br/>                | <span data-ttu-id="ef707-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ef707-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ef707-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ef707-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef707-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef707-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef707-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef707-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef707-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef707-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef707-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef707-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef707-147">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="ef707-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

