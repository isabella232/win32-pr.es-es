---
title: Método FetchReportEntries de la clase Win32_TSLicenseReport
description: Recupera los detalles de las licencias de acceso de cliente de Servicios de Escritorio remoto por usuario (RDS \ 160; Cal por usuario) del informe. Cada entrada representa un RDS \ 160; CAL por usuario que está actualmente en uso.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Método FetchReportEntries Servicios de Escritorio remoto
- Método FetchReportEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535235"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="9258c-107">Método FetchReportEntries de la \_ clase TSLicenseReport de Win32</span><span class="sxs-lookup"><span data-stu-id="9258c-107">FetchReportEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="9258c-108">Recupera detalles de las licencias de acceso de cliente de Servicios de Escritorio remoto por usuario (cal por usuario de RDS) del informe.</span><span class="sxs-lookup"><span data-stu-id="9258c-108">Retrieves details of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span> <span data-ttu-id="9258c-109">Cada entrada representa una CAL por usuario de RDS que está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="9258c-109">Each entry represents a RDS Per User CAL that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="9258c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9258c-110">Syntax</span></span>


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="9258c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9258c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9258c-112">*StartIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9258c-112">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9258c-113">Índice de la primera entrada del informe que se va a recibir.</span><span class="sxs-lookup"><span data-stu-id="9258c-113">Index of the first report entry to be received.</span></span> <span data-ttu-id="9258c-114">La primera entrada del informe tiene un índice de cero.</span><span class="sxs-lookup"><span data-stu-id="9258c-114">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="9258c-115">*Recuento* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9258c-115">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9258c-116">Número de entradas de informe que se van a recuperar del objeto de informe.</span><span class="sxs-lookup"><span data-stu-id="9258c-116">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="9258c-117">Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* .</span><span class="sxs-lookup"><span data-stu-id="9258c-117">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="9258c-118">En la devolución, contiene el número de entradas de la matriz *ReportEntries* .</span><span class="sxs-lookup"><span data-stu-id="9258c-118">On return, contains the number of entries in the *ReportEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="9258c-119">*ReportEntries* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9258c-119">*ReportEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9258c-120">Devuelve una matriz de [**clases \_ TSLicenseReportEntry de Win32**](win32-tslicensereportentry.md) .</span><span class="sxs-lookup"><span data-stu-id="9258c-120">Returns an array of [**Win32\_TSLicenseReportEntry**](win32-tslicensereportentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9258c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9258c-121">Return value</span></span>

<span data-ttu-id="9258c-122">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9258c-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9258c-123">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9258c-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9258c-124">Un valor de **LSERVER \_ I \_ no hay \_ más \_ datos** (0x4001) indica que no hay más entradas de informe.</span><span class="sxs-lookup"><span data-stu-id="9258c-124">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="9258c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9258c-125">Remarks</span></span>

<span data-ttu-id="9258c-126">No es un método estático.</span><span class="sxs-lookup"><span data-stu-id="9258c-126">This is not a static method.</span></span> <span data-ttu-id="9258c-127">Se debe llamar a este método desde un objeto de informe de uso de licencias por usuario.</span><span class="sxs-lookup"><span data-stu-id="9258c-127">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="9258c-128">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="9258c-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9258c-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9258c-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9258c-130">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9258c-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9258c-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="9258c-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9258c-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9258c-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9258c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9258c-133">Requirements</span></span>



| <span data-ttu-id="9258c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9258c-134">Requirement</span></span> | <span data-ttu-id="9258c-135">Value</span><span class="sxs-lookup"><span data-stu-id="9258c-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9258c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9258c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9258c-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9258c-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9258c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9258c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9258c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9258c-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9258c-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9258c-140">Namespace</span></span><br/>                | <span data-ttu-id="9258c-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9258c-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9258c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9258c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9258c-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9258c-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9258c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9258c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9258c-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9258c-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9258c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="9258c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9258c-147">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="9258c-147">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="9258c-148">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="9258c-148">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

