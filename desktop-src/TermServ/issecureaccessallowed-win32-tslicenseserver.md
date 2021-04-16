---
title: Método IsSecureAccessAllowed de la clase Win32_TSLicenseServer
description: Recupera si se permite que un servidor host de sesión de escritorio remoto (host de sesión Escritorio remoto de RD) solicite Servicios de Escritorio remoto licencias de acceso de cliente (RDS \ 160; Cal) del servidor de licencias de Escritorio remoto.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Método IsSecureAccessAllowed Servicios de Escritorio remoto
- Método IsSecureAccessAllowed Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534126"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f4e16-106">Método IsSecureAccessAllowed de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="f4e16-106">IsSecureAccessAllowed method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f4e16-107">Recupera si se permite que un servidor host de sesión de escritorio remoto (host de sesión Escritorio remoto de RD) solicite Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f4e16-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e16-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4e16-108">Syntax</span></span>


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="f4e16-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4e16-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e16-110">*tsname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4e16-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e16-111">Nombre del servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f4e16-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="f4e16-112">*Permitido* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f4e16-112">*Allowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e16-113">Valor booleano que indica si el servidor host de sesión de escritorio remoto puede solicitar cal de RDS del servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="f4e16-113">Boolean value that indicates whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e16-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4e16-114">Return value</span></span>

<span data-ttu-id="f4e16-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f4e16-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f4e16-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f4e16-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f4e16-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f4e16-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e16-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4e16-118">Remarks</span></span>

<span data-ttu-id="f4e16-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="f4e16-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f4e16-120">El valor devuelto se basa en la configuración de directiva de grupo "grupo de seguridad del servidor de licencias" y la pertenencia al grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f4e16-120">The returned value is based on the "license server security group" group policy setting, and membership in the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

<span data-ttu-id="f4e16-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f4e16-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f4e16-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f4e16-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f4e16-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f4e16-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f4e16-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f4e16-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e16-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4e16-125">Requirements</span></span>



| <span data-ttu-id="f4e16-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e16-126">Requirement</span></span> | <span data-ttu-id="f4e16-127">Value</span><span class="sxs-lookup"><span data-stu-id="f4e16-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e16-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4e16-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e16-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f4e16-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f4e16-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4e16-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e16-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4e16-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f4e16-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4e16-132">Namespace</span></span><br/>                | <span data-ttu-id="f4e16-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f4e16-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f4e16-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f4e16-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4e16-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4e16-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4e16-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4e16-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4e16-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4e16-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e16-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4e16-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e16-139">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f4e16-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="f4e16-140">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="f4e16-140">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

