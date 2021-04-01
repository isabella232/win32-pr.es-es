---
title: Método FetchReportSummaryEntries de la clase Win32_TSLicenseReport
description: Recupera resúmenes de las licencias de acceso de cliente de Servicios de Escritorio remoto por usuario (RDS \ 160; Cal por usuario) del informe.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Método FetchReportSummaryEntries Servicios de Escritorio remoto
- Método FetchReportSummaryEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149958"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="d3222-106">Método FetchReportSummaryEntries de la \_ clase TSLicenseReport de Win32</span><span class="sxs-lookup"><span data-stu-id="d3222-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="d3222-107">Recupera resúmenes de Servicios de Escritorio remoto licencias de acceso de cliente por usuario (cal por usuario de RDS) del informe.</span><span class="sxs-lookup"><span data-stu-id="d3222-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3222-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3222-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="d3222-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3222-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3222-110">*StartIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3222-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3222-111">Índice de la primera entrada del informe que se va a recibir.</span><span class="sxs-lookup"><span data-stu-id="d3222-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="d3222-112">La primera entrada del informe tiene un índice de cero.</span><span class="sxs-lookup"><span data-stu-id="d3222-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="d3222-113">*Recuento* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d3222-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3222-114">Número de entradas de informe que se van a recuperar del objeto de informe.</span><span class="sxs-lookup"><span data-stu-id="d3222-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="d3222-115">Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* .</span><span class="sxs-lookup"><span data-stu-id="d3222-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="d3222-116">En la devolución, contiene el número de entradas de la matriz *ReportSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="d3222-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="d3222-117">*ReportSummaryEntries* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d3222-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3222-118">Devuelve una matriz de [**clases \_ TSLicenseReportSummaryEntry de Win32**](win32-tslicensereportsummaryentry.md) .</span><span class="sxs-lookup"><span data-stu-id="d3222-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3222-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3222-119">Return value</span></span>

<span data-ttu-id="d3222-120">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d3222-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d3222-121">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d3222-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d3222-122">Un valor de **LSERVER \_ I \_ no hay \_ más \_ datos** (0x4001) indica que no hay más entradas de informe.</span><span class="sxs-lookup"><span data-stu-id="d3222-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3222-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3222-123">Remarks</span></span>

<span data-ttu-id="d3222-124">No es un método estático.</span><span class="sxs-lookup"><span data-stu-id="d3222-124">This is not a static method.</span></span> <span data-ttu-id="d3222-125">Se debe llamar a este método desde un objeto de informe de uso de licencias por usuario.</span><span class="sxs-lookup"><span data-stu-id="d3222-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="d3222-126">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d3222-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d3222-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3222-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3222-128">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d3222-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d3222-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d3222-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3222-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d3222-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3222-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3222-131">Requirements</span></span>



| <span data-ttu-id="d3222-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3222-132">Requirement</span></span> | <span data-ttu-id="d3222-133">Value</span><span class="sxs-lookup"><span data-stu-id="d3222-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3222-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3222-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d3222-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d3222-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d3222-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3222-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d3222-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3222-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d3222-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3222-138">Namespace</span></span><br/>                | <span data-ttu-id="d3222-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d3222-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d3222-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d3222-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3222-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3222-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3222-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3222-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3222-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3222-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3222-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3222-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3222-145">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="d3222-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="d3222-146">**Win32 \_ TSLicenseReportSummaryEntry**</span><span class="sxs-lookup"><span data-stu-id="d3222-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

