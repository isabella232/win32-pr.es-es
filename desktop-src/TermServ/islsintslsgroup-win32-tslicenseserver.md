---
title: Método IsLSinTSLSGroup de la clase Win32_TSLicenseServer
description: Recupera si el servidor de licencias de Escritorio remoto es miembro del grupo de servidores de licencias de Escritorio remoto en un controlador de dominio de un dominio determinado.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Método IsLSinTSLSGroup Servicios de Escritorio remoto
- Método IsLSinTSLSGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676815"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="60107-106">Método IsLSinTSLSGroup de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="60107-106">IsLSinTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="60107-107">Recupera si el servidor de licencias de Escritorio remoto es miembro del grupo de servidores de licencias de Escritorio remoto en un controlador de dominio de un dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="60107-107">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop license server group on a domain controller in a given domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="60107-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60107-108">Syntax</span></span>


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="60107-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60107-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60107-110">*Dominio* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="60107-110">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60107-111">Nombre del dominio.</span><span class="sxs-lookup"><span data-stu-id="60107-111">The domain name.</span></span>

</dd> <dt>

<span data-ttu-id="60107-112">*IsMember* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60107-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60107-113">Valor booleano que indica si el servidor de licencias es miembro del grupo de servidores de licencias Escritorio remoto en el dominio.</span><span class="sxs-lookup"><span data-stu-id="60107-113">Boolean value that indicates whether the license server is a member of the Remote Desktop license server group in the domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60107-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60107-114">Return value</span></span>

<span data-ttu-id="60107-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="60107-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="60107-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="60107-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="60107-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="60107-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60107-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60107-118">Remarks</span></span>

<span data-ttu-id="60107-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="60107-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="60107-120">Si no se proporciona ningún nombre de dominio, se consulta un controlador de dominio en el mismo dominio que el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="60107-120">If no domain name is provided, a domain controller in the same domain as the license server is queried.</span></span>

<span data-ttu-id="60107-121">El servidor de licencias debe ser miembro del grupo de servidores de licencias de Escritorio remoto si el servidor está configurado para utilizar el ámbito de detección de dominio o bosque.</span><span class="sxs-lookup"><span data-stu-id="60107-121">The license server should be a member of the Remote Desktop license server group if the server is configured to use the domain or forest discovery scope.</span></span> <span data-ttu-id="60107-122">Si el servidor de licencias no es miembro de este grupo, el seguimiento de licencias por usuario y los informes no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="60107-122">If the license server is not a member of this group, per-user license tracking and reporting will not work.</span></span>

<span data-ttu-id="60107-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="60107-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60107-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60107-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60107-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="60107-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60107-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60107-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60107-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60107-127">Requirements</span></span>



| <span data-ttu-id="60107-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="60107-128">Requirement</span></span> | <span data-ttu-id="60107-129">Value</span><span class="sxs-lookup"><span data-stu-id="60107-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60107-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60107-130">Minimum supported client</span></span><br/> | <span data-ttu-id="60107-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60107-131">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="60107-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60107-132">Minimum supported server</span></span><br/> | <span data-ttu-id="60107-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60107-133">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="60107-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60107-134">Namespace</span></span><br/>                | <span data-ttu-id="60107-135">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="60107-135">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="60107-136">MOF</span><span class="sxs-lookup"><span data-stu-id="60107-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60107-137"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60107-137"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="60107-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60107-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60107-139"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60107-139"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60107-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="60107-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60107-141">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="60107-141">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="60107-142">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="60107-142">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="60107-143">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="60107-143">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

