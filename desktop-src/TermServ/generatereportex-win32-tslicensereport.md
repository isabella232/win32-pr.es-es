---
title: Método GenerateReportEx de la clase Win32_TSLicenseReport
description: Genera un informe de uso de licencias actual para licencias por usuario y por dispositivo.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Método GenerateReportEx Servicios de Escritorio remoto
- Método GenerateReportEx Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método GenerateReportEx
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422012"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="c7750-106">Método GenerateReportEx de la \_ clase TSLicenseReport de Win32</span><span class="sxs-lookup"><span data-stu-id="c7750-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="c7750-107">Genera un informe de uso de licencias actual para licencias por usuario y por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7750-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7750-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7750-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="c7750-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7750-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7750-110">*Nombre de archivo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7750-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7750-111">Nombre de archivo del informe generado.</span><span class="sxs-lookup"><span data-stu-id="c7750-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7750-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7750-112">Return value</span></span>

<span data-ttu-id="c7750-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c7750-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c7750-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c7750-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c7750-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c7750-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7750-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7750-116">Remarks</span></span>

<span data-ttu-id="c7750-117">Se trata de un método estático.</span><span class="sxs-lookup"><span data-stu-id="c7750-117">This is a static method.</span></span>

<span data-ttu-id="c7750-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="c7750-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c7750-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c7750-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c7750-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c7750-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c7750-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c7750-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c7750-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c7750-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7750-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7750-123">Requirements</span></span>



| <span data-ttu-id="c7750-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7750-124">Requirement</span></span> | <span data-ttu-id="c7750-125">Value</span><span class="sxs-lookup"><span data-stu-id="c7750-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7750-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7750-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7750-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c7750-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c7750-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7750-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7750-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7750-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="c7750-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7750-130">Namespace</span></span><br/>                | <span data-ttu-id="c7750-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c7750-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c7750-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c7750-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7750-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7750-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7750-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7750-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7750-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7750-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7750-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7750-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7750-137">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="c7750-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

