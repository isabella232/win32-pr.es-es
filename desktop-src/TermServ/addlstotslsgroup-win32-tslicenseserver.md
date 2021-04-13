---
title: Método AddLStoTSLSGroup de la clase Win32_TSLicenseServer
description: Agrega el servidor de licencias de Escritorio remoto al grupo servidores de licencias de agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto) en un controlador de dominio del mismo dominio que el servidor de licencias de Escritorio remoto.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Método AddLStoTSLSGroup Servicios de Escritorio remoto
- Método AddLStoTSLSGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422153"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="49d71-106">Método AddLStoTSLSGroup de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="49d71-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="49d71-107">Agrega el servidor de licencias de Escritorio remoto al grupo servidores de licencias de agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto) en un controlador de dominio del mismo dominio que el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="49d71-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49d71-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49d71-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="49d71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49d71-109">Parameters</span></span>

<span data-ttu-id="49d71-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="49d71-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49d71-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49d71-111">Return value</span></span>

<span data-ttu-id="49d71-112">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="49d71-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="49d71-113">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="49d71-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="49d71-114">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="49d71-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49d71-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49d71-115">Remarks</span></span>

<span data-ttu-id="49d71-116">Para llamar a este método, debe ser miembro del grupo Admins. del dominio.</span><span class="sxs-lookup"><span data-stu-id="49d71-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="49d71-117">El servidor de licencias debe ser miembro del grupo servidores de licencias de Escritorio remoto si el servidor está configurado para utilizar el ámbito de detección de dominio o bosque.</span><span class="sxs-lookup"><span data-stu-id="49d71-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="49d71-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="49d71-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="49d71-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="49d71-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="49d71-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="49d71-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="49d71-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="49d71-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="49d71-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d71-122">Requirements</span></span>



| <span data-ttu-id="49d71-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d71-123">Requirement</span></span> | <span data-ttu-id="49d71-124">Value</span><span class="sxs-lookup"><span data-stu-id="49d71-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="49d71-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49d71-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49d71-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49d71-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="49d71-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49d71-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49d71-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49d71-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="49d71-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="49d71-129">Namespace</span></span><br/>                | <span data-ttu-id="49d71-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="49d71-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="49d71-131">MOF</span><span class="sxs-lookup"><span data-stu-id="49d71-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49d71-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49d71-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="49d71-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49d71-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49d71-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49d71-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d71-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="49d71-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d71-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="49d71-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="49d71-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="49d71-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

