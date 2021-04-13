---
title: Win32_RDMSJoinedNode (clase)
description: Representa un nodo de servidor administrado por Escritorio remoto Management Services (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSJoinedNode de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421965"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="bfefe-105">\_Clase Win32 RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="bfefe-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="bfefe-106">Representa un nodo de servidor administrado por Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="bfefe-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="bfefe-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bfefe-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfefe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfefe-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="bfefe-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bfefe-109">Members</span></span>

<span data-ttu-id="bfefe-110">La **clase \_ RDMSJoinedNode de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bfefe-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="bfefe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bfefe-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bfefe-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfefe-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bfefe-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bfefe-113">Methods</span></span>

<span data-ttu-id="bfefe-114">La clase **Win32 \_ RDMSJoinedNode** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bfefe-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="bfefe-115">Método</span><span class="sxs-lookup"><span data-stu-id="bfefe-115">Method</span></span>                                                                | <span data-ttu-id="bfefe-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfefe-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfefe-117">**GetJoinedNodeCount**</span><span class="sxs-lookup"><span data-stu-id="bfefe-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="bfefe-118">**Windows server 2012 R2 y Windows server 2012:** Este método no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="bfefe-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="bfefe-119">Obtiene el número de servidores que tienen el rol especificado instalado.</span><span class="sxs-lookup"><span data-stu-id="bfefe-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="bfefe-120">**Combinar**</span><span class="sxs-lookup"><span data-stu-id="bfefe-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="bfefe-121">Agrega un nodo a RDMS.</span><span class="sxs-lookup"><span data-stu-id="bfefe-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="bfefe-122">**Separarse**</span><span class="sxs-lookup"><span data-stu-id="bfefe-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="bfefe-123">Quita un nodo de RDMS.</span><span class="sxs-lookup"><span data-stu-id="bfefe-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="bfefe-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfefe-124">Properties</span></span>

<span data-ttu-id="bfefe-125">La **clase \_ RDMSJoinedNode de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bfefe-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfefe-126">**FQDN**</span><span class="sxs-lookup"><span data-stu-id="bfefe-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfefe-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfefe-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-129">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bfefe-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-130">Obtiene el nombre de dominio completo del nodo.</span><span class="sxs-lookup"><span data-stu-id="bfefe-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-131">**IsGatewayCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="bfefe-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-132">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-134">Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para Escritorio remoto conexiones de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="bfefe-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="bfefe-135">**True** si el certificado está instalado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-136">**IsPublishingCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="bfefe-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-139">Obtiene y establece un valor que indica si el servidor tiene un certificado para firmar Protocolo de escritorio remoto archivos de publicación.</span><span class="sxs-lookup"><span data-stu-id="bfefe-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="bfefe-140">**True** si el certificado está instalado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-141">**IsRdcb**</span><span class="sxs-lookup"><span data-stu-id="bfefe-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-144">Obtiene y establece un valor que indica si el servidor está Conexión a Escritorio remoto Broker.</span><span class="sxs-lookup"><span data-stu-id="bfefe-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="bfefe-145">**True** si el servidor es un agente de conexión a escritorio remoto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-146">**IsRdg**</span><span class="sxs-lookup"><span data-stu-id="bfefe-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-149">Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="bfefe-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="bfefe-150">**True** si el servidor es un servidor de puerta de enlace de escritorio remoto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-151">**IsRdls**</span><span class="sxs-lookup"><span data-stu-id="bfefe-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-152">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-154">Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="bfefe-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="bfefe-155">**True** si el servidor es un servidor de licencias de escritorio remoto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-156">**IsRdsh**</span><span class="sxs-lookup"><span data-stu-id="bfefe-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-157">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-159">Obtiene y establece un valor que indica si el servidor es Escritorio remoto servidor host de sesión.</span><span class="sxs-lookup"><span data-stu-id="bfefe-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="bfefe-160">**True** si el servidor es un servidor host de sesión escritorio remoto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-161">**IsRdvh**</span><span class="sxs-lookup"><span data-stu-id="bfefe-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-162">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-164">Obtiene y establece un valor que indica si el servidor está Escritorio remoto host de virtualización.</span><span class="sxs-lookup"><span data-stu-id="bfefe-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="bfefe-165">**True** si el servidor es un host de virtualización de escritorio remoto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-166">**IsRdwa**</span><span class="sxs-lookup"><span data-stu-id="bfefe-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-167">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-169">Obtiene y establece un valor que indica si el servidor está Escritorio remoto servidor de acceso web.</span><span class="sxs-lookup"><span data-stu-id="bfefe-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="bfefe-170">**True** si el servidor es un servidor de escritorio remoto Web Access; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-171">**IsRedirectorCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="bfefe-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-174">Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para Servicios de Escritorio remoto implementación.</span><span class="sxs-lookup"><span data-stu-id="bfefe-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="bfefe-175">**True** si el certificado está instalado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-176">**IsWebAccessCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="bfefe-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-177">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bfefe-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-179">Obtiene y establece un valor que indica si el servidor tiene un certificado para realizar la autenticación para Escritorio remoto acceso web.</span><span class="sxs-lookup"><span data-stu-id="bfefe-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="bfefe-180">**True** si el certificado está instalado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfefe-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="bfefe-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfefe-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-183">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bfefe-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-184">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bfefe-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-185">Obtiene y establece la versión de los sistemas operativos en el nodo.</span><span class="sxs-lookup"><span data-stu-id="bfefe-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="bfefe-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="bfefe-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfefe-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfefe-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfefe-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfefe-189">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bfefe-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bfefe-190">Obtiene el identificador de seguridad (SID) del nodo.</span><span class="sxs-lookup"><span data-stu-id="bfefe-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfefe-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfefe-191">Requirements</span></span>



| <span data-ttu-id="bfefe-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfefe-192">Requirement</span></span> | <span data-ttu-id="bfefe-193">Value</span><span class="sxs-lookup"><span data-stu-id="bfefe-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfefe-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfefe-194">Minimum supported client</span></span><br/> | <span data-ttu-id="bfefe-195">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bfefe-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="bfefe-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfefe-196">Minimum supported server</span></span><br/> | <span data-ttu-id="bfefe-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfefe-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="bfefe-198">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bfefe-198">Namespace</span></span><br/>                | <span data-ttu-id="bfefe-199">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="bfefe-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="bfefe-200">MOF</span><span class="sxs-lookup"><span data-stu-id="bfefe-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfefe-201"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfefe-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfefe-202">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfefe-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfefe-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfefe-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="bfefe-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfefe-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfefe-205">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="bfefe-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

