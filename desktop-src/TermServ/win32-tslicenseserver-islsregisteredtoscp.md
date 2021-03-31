---
title: Método IsLSRegisteredToSCP de la clase Win32_TSLicenseServer
description: Recupera si el servidor de licencias de Escritorio remoto está registrado como punto de conexión de servicio en Active Directory Domain Services.
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- Método IsLSRegisteredToSCP Servicios de Escritorio remoto
- Método IsLSRegisteredToSCP Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSRegisteredToSCP
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b203ff580c5ff8871d023c7f349626acdd693f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801291"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a6ae0-106">Método IsLSRegisteredToSCP de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="a6ae0-106">IsLSRegisteredToSCP method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a6ae0-107">Recupera si el servidor de licencias de Escritorio remoto está registrado como punto de conexión de servicio en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-107">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ae0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6ae0-108">Syntax</span></span>


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a><span data-ttu-id="a6ae0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6ae0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ae0-110">*Registrado* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a6ae0-110">*Registered* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ae0-111">Valor booleano que indica si el servidor de licencias de Escritorio remoto está registrado como punto de conexión de servicio en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-111">Boolean value that indicates whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ae0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6ae0-112">Return value</span></span>

<span data-ttu-id="a6ae0-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a6ae0-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a6ae0-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a6ae0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6ae0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6ae0-116">Remarks</span></span>

<span data-ttu-id="a6ae0-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a6ae0-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a6ae0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a6ae0-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a6ae0-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a6ae0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a6ae0-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a6ae0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ae0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6ae0-122">Requirements</span></span>



| <span data-ttu-id="a6ae0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ae0-123">Requirement</span></span> | <span data-ttu-id="a6ae0-124">Value</span><span class="sxs-lookup"><span data-stu-id="a6ae0-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ae0-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6ae0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ae0-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a6ae0-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a6ae0-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6ae0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ae0-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6ae0-128">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="a6ae0-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6ae0-129">Namespace</span></span><br/>                | <span data-ttu-id="a6ae0-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a6ae0-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a6ae0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a6ae0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6ae0-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae0-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6ae0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6ae0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ae0-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae0-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ae0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6ae0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ae0-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="a6ae0-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

