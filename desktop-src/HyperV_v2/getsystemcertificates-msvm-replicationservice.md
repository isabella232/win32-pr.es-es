---
description: Recupera los certificados del sistema en un sistema host.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Método GetSystemCertificates de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540347"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="0ad15-103">Método GetSystemCertificates de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="0ad15-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="0ad15-104">Recupera los certificados del sistema en un sistema host.</span><span class="sxs-lookup"><span data-stu-id="0ad15-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ad15-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="0ad15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ad15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad15-107">*EncodedCertificates* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ad15-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad15-108">Si se realiza correctamente, recibe los certificados disponibles en el almacén personal del equipo local.</span><span class="sxs-lookup"><span data-stu-id="0ad15-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="0ad15-109">Cada entrada es una cadena de certificado codificada en base 64.</span><span class="sxs-lookup"><span data-stu-id="0ad15-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="0ad15-110">Esta cadena se puede convertir en una matriz de bytes mediante la construcción de un objeto X509Certificate2.</span><span class="sxs-lookup"><span data-stu-id="0ad15-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad15-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ad15-111">Return value</span></span>

<span data-ttu-id="0ad15-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ad15-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0ad15-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0ad15-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0ad15-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="0ad15-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0ad15-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="0ad15-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0ad15-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="0ad15-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0ad15-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0ad15-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="0ad15-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0ad15-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0ad15-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0ad15-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0ad15-126">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="0ad15-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0ad15-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ad15-127">Requirements</span></span>



| <span data-ttu-id="0ad15-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad15-128">Requirement</span></span> | <span data-ttu-id="0ad15-129">Value</span><span class="sxs-lookup"><span data-stu-id="0ad15-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad15-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ad15-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad15-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ad15-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ad15-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ad15-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad15-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ad15-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ad15-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ad15-134">Namespace</span></span><br/>                | <span data-ttu-id="0ad15-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0ad15-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ad15-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0ad15-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ad15-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ad15-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ad15-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ad15-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ad15-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ad15-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ad15-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ad15-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad15-141">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="0ad15-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




