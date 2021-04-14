---
title: Método DeleteReport de la clase Win32_TSLicenseReport
description: Elimina un objeto de informe en el servidor de licencias de Escritorio remoto. No es un método estático.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Método DeleteReport Servicios de Escritorio remoto
- Método DeleteReport Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método DeleteReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533837"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="fec79-107">Método DeleteReport de la \_ clase TSLicenseReport de Win32</span><span class="sxs-lookup"><span data-stu-id="fec79-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="fec79-108">Elimina un objeto de informe en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fec79-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="fec79-109">No es un método estático.</span><span class="sxs-lookup"><span data-stu-id="fec79-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec79-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fec79-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="fec79-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fec79-111">Parameters</span></span>

<span data-ttu-id="fec79-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fec79-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fec79-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fec79-113">Return value</span></span>

<span data-ttu-id="fec79-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="fec79-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fec79-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fec79-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fec79-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fec79-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fec79-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fec79-117">Remarks</span></span>

<span data-ttu-id="fec79-118">No es un método estático.</span><span class="sxs-lookup"><span data-stu-id="fec79-118">This is not a static method.</span></span> <span data-ttu-id="fec79-119">Se debe llamar a este método desde un objeto de informe de uso de licencias por usuario.</span><span class="sxs-lookup"><span data-stu-id="fec79-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="fec79-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="fec79-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fec79-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fec79-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fec79-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fec79-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fec79-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fec79-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fec79-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fec79-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fec79-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec79-125">Requirements</span></span>



| <span data-ttu-id="fec79-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec79-126">Requirement</span></span> | <span data-ttu-id="fec79-127">Value</span><span class="sxs-lookup"><span data-stu-id="fec79-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec79-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fec79-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fec79-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fec79-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fec79-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fec79-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fec79-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fec79-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fec79-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fec79-132">Namespace</span></span><br/>                | <span data-ttu-id="fec79-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fec79-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fec79-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fec79-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fec79-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fec79-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fec79-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fec79-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fec79-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fec79-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec79-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="fec79-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec79-139">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="fec79-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

