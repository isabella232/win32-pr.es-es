---
title: Método UnRegisterLSFromSCP de la clase Win32_TSLicenseServer
description: Quita el servidor de licencias de Escritorio remoto como punto de conexión de servicio en Active Directory Domain Services.
ms.assetid: 3EE6F272-A99F-49EF-BDED-D8C2C641D45B
ms.tgt_platform: multiple
keywords:
- Método UnRegisterLSFromSCP Servicios de Escritorio remoto
- Método UnRegisterLSFromSCP Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método UnRegisterLSFromSCP
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnRegisterLSFromSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d365b0f3e64c57fba9447d8658c3a955b6e92f73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676705"
---
# <a name="unregisterlsfromscp-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a651a-106">Método UnRegisterLSFromSCP de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="a651a-106">UnRegisterLSFromSCP method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a651a-107">Quita el servidor de licencias de Escritorio remoto como punto de conexión de servicio en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a651a-107">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="a651a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a651a-108">Syntax</span></span>


```mof
uint32 UnRegisterLSFromSCP();
```



## <a name="parameters"></a><span data-ttu-id="a651a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a651a-109">Parameters</span></span>

<span data-ttu-id="a651a-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a651a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a651a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a651a-111">Return value</span></span>

<span data-ttu-id="a651a-112">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a651a-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a651a-113">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a651a-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a651a-114">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a651a-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a651a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a651a-115">Remarks</span></span>

<span data-ttu-id="a651a-116">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="a651a-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a651a-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a651a-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a651a-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a651a-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a651a-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a651a-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a651a-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a651a-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a651a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a651a-121">Requirements</span></span>



| <span data-ttu-id="a651a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a651a-122">Requirement</span></span> | <span data-ttu-id="a651a-123">Value</span><span class="sxs-lookup"><span data-stu-id="a651a-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a651a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a651a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a651a-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a651a-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a651a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a651a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a651a-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a651a-127">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="a651a-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a651a-128">Namespace</span></span><br/>                | <span data-ttu-id="a651a-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a651a-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a651a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a651a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a651a-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a651a-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a651a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a651a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a651a-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a651a-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a651a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a651a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a651a-135">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="a651a-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

