---
title: Win32_TSLicenseReportFailedPerUserSummaryEntry (clase)
description: Proporciona detalles de los dominios en los que se produjo un error en la emisión por usuario.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserSummaryEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportFailedPerUserSummaryEntry de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995991"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="42d41-105">\_Clase Win32 TSLicenseReportFailedPerUserSummaryEntry</span><span class="sxs-lookup"><span data-stu-id="42d41-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="42d41-106">Proporciona detalles de los dominios en los que se produjo un error en la emisión por usuario.</span><span class="sxs-lookup"><span data-stu-id="42d41-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="42d41-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="42d41-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d41-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42d41-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="42d41-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="42d41-109">Members</span></span>

<span data-ttu-id="42d41-110">La **clase \_ TSLicenseReportFailedPerUserSummaryEntry de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42d41-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="42d41-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42d41-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42d41-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42d41-112">Properties</span></span>

<span data-ttu-id="42d41-113">La **clase \_ TSLicenseReportFailedPerUserSummaryEntry de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42d41-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42d41-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="42d41-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d41-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42d41-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42d41-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42d41-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42d41-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42d41-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42d41-118">Especifica el nombre de dominio en el que se produjo el error de emisión de licencias.</span><span class="sxs-lookup"><span data-stu-id="42d41-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="42d41-119">**FailedIssuanceCount**</span><span class="sxs-lookup"><span data-stu-id="42d41-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d41-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42d41-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42d41-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42d41-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42d41-122">El número de emisiones erróneas.</span><span class="sxs-lookup"><span data-stu-id="42d41-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42d41-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d41-123">Requirements</span></span>



| <span data-ttu-id="42d41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d41-124">Requirement</span></span> | <span data-ttu-id="42d41-125">Value</span><span class="sxs-lookup"><span data-stu-id="42d41-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d41-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42d41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42d41-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="42d41-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="42d41-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42d41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42d41-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42d41-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="42d41-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42d41-130">Namespace</span></span><br/>                | <span data-ttu-id="42d41-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="42d41-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="42d41-132">MOF</span><span class="sxs-lookup"><span data-stu-id="42d41-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42d41-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42d41-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="42d41-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42d41-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42d41-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42d41-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d41-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="42d41-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d41-137">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="42d41-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

