---
description: Comprueba si la replicación se puede habilitar desde el sistema host actual al sistema de recuperación especificado.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Método TestReplicationConnection de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666309"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d7dd7-103">Método TestReplicationConnection de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="d7dd7-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d7dd7-104">Comprueba si la replicación se puede habilitar desde el sistema host actual al sistema de recuperación especificado.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7dd7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7dd7-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d7dd7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7dd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7dd7-107">*RecoveryConnectionPoint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7dd7-108">Nombre del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-108">The name of the connection point.</span></span> <span data-ttu-id="d7dd7-109">Para un clúster de recuperación, este es el nombre de la CAP de agente.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="d7dd7-110">Para un servidor de recuperación independiente, es el nombre del sistema host.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="d7dd7-111">*RecoveryServerPortNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7dd7-112">Número de puerto del punto de conexión de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="d7dd7-113">*AuthenticationType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7dd7-114">El esquema de autenticación de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-114">The recovery authentication scheme.</span></span> <span data-ttu-id="d7dd7-115">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="d7dd7-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Autenticación integrada** (1)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d7dd7-117">Autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="d7dd7-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticación basada en certificados** (2)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d7dd7-119">Autenticación basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d7dd7-120">*CertificateThumbPrint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7dd7-121">Huella digital del certificado que se usará cuando el parámetro *AuthenticationType* sea autenticación basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="d7dd7-122">*BypassProxyServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7dd7-123">Omitir el servidor proxy al conectarse al servidor réplica.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="d7dd7-124">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7dd7-125">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d7dd7-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7dd7-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7dd7-126">Return value</span></span>

<span data-ttu-id="d7dd7-127">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d7dd7-128">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-129">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-130">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-131">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-132">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-133">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-134">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-135">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-136">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-137">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-138">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-139">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-140">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d7dd7-141">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d7dd7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7dd7-142">Requirements</span></span>



| <span data-ttu-id="d7dd7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7dd7-143">Requirement</span></span> | <span data-ttu-id="d7dd7-144">Value</span><span class="sxs-lookup"><span data-stu-id="d7dd7-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7dd7-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7dd7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d7dd7-146">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d7dd7-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7dd7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d7dd7-148">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7dd7-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7dd7-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d7dd7-149">Namespace</span></span><br/>                | <span data-ttu-id="d7dd7-150">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d7dd7-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d7dd7-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d7dd7-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7dd7-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd7-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7dd7-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7dd7-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7dd7-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd7-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7dd7-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7dd7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7dd7-156">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

