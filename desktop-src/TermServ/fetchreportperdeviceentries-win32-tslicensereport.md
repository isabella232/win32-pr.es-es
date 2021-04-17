---
title: Método FetchReportPerDeviceEntries de la clase Win32_TSLicenseReport
description: Recupera información de las licencias de acceso de cliente por dispositivo Servicios de Escritorio remoto emitidas (RDS \ 160; Cal por dispositivo) del informe.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Método FetchReportPerDeviceEntries Servicios de Escritorio remoto
- Método FetchReportPerDeviceEntries Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676937"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="2eae7-106">Método FetchReportPerDeviceEntries de la \_ clase TSLicenseReport de Win32</span><span class="sxs-lookup"><span data-stu-id="2eae7-106">FetchReportPerDeviceEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="2eae7-107">Recupera la información de las licencias de acceso de cliente por dispositivo de Servicios de Escritorio remoto emitidas (cal por dispositivo de RDS) del informe.</span><span class="sxs-lookup"><span data-stu-id="2eae7-107">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eae7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eae7-108">Syntax</span></span>


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="2eae7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eae7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eae7-110">*StartIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eae7-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eae7-111">Índice de la primera entrada del informe que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="2eae7-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="2eae7-112">La primera entrada del informe tiene un índice de cero.</span><span class="sxs-lookup"><span data-stu-id="2eae7-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="2eae7-113">*Recuento* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2eae7-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eae7-114">Número de entradas de informe que se van a recuperar del objeto de informe.</span><span class="sxs-lookup"><span data-stu-id="2eae7-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="2eae7-115">Un valor de cero indica que se recuperarán todas las entradas del informe que comienzan en *StartIndex* .</span><span class="sxs-lookup"><span data-stu-id="2eae7-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="2eae7-116">En la devolución, contiene el número de entradas de la matriz *ReportPerDeviceEntries* .</span><span class="sxs-lookup"><span data-stu-id="2eae7-116">On return, contains the number of entries in the *ReportPerDeviceEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="2eae7-117">*ReportPerDeviceEntries* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2eae7-117">*ReportPerDeviceEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eae7-118">Matriz de clases [**\_ TSLicenseReportPerDeviceEntry de Win32**](win32-tslicensereportperdeviceentry.md) que representan las entradas de licencia recuperadas.</span><span class="sxs-lookup"><span data-stu-id="2eae7-118">An array of [**Win32\_TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) classes the represent the license entries retrieved.</span></span> <span data-ttu-id="2eae7-119">El parámetro *Count* contiene el número de elementos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="2eae7-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eae7-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eae7-120">Return value</span></span>

<span data-ttu-id="2eae7-121">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2eae7-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2eae7-122">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2eae7-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2eae7-123">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2eae7-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2eae7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eae7-124">Requirements</span></span>



| <span data-ttu-id="2eae7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eae7-125">Requirement</span></span> | <span data-ttu-id="2eae7-126">Value</span><span class="sxs-lookup"><span data-stu-id="2eae7-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eae7-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eae7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2eae7-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2eae7-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2eae7-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eae7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2eae7-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2eae7-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="2eae7-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2eae7-131">Namespace</span></span><br/>                | <span data-ttu-id="2eae7-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2eae7-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2eae7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2eae7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eae7-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eae7-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eae7-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2eae7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eae7-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eae7-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eae7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eae7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eae7-138">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="2eae7-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





