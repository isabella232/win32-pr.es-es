---
title: Win32_TSGatewayServer (clase)
description: Se usa para las operaciones específicas del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490276"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="b6359-105">\_Clase Win32 TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="b6359-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="b6359-106">Se usa para las operaciones específicas del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="b6359-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6359-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6359-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="b6359-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6359-108">Members</span></span>

<span data-ttu-id="b6359-109">La **clase \_ TSGatewayServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6359-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="b6359-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6359-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b6359-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6359-111">Methods</span></span>

<span data-ttu-id="b6359-112">La clase **Win32 \_ TSGatewayServer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b6359-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="b6359-113">Método</span><span class="sxs-lookup"><span data-stu-id="b6359-113">Method</span></span>                                                                                   | <span data-ttu-id="b6359-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6359-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6359-115">**CreateSelfSignedCertificate**</span><span class="sxs-lookup"><span data-stu-id="b6359-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="b6359-116">Crea un certificado autofirmado con un nombre de sujeto determinado y devuelve el hash del certificado como un parámetro "out".</span><span class="sxs-lookup"><span data-stu-id="b6359-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="b6359-117">**Exportación**</span><span class="sxs-lookup"><span data-stu-id="b6359-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="b6359-118">Devuelve la configuración del servidor de puerta de enlace de escritorio remoto como una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="b6359-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="b6359-119">**Importar**</span><span class="sxs-lookup"><span data-stu-id="b6359-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="b6359-120">Importa una configuración determinada en el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b6359-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="b6359-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6359-121">Remarks</span></span>

<span data-ttu-id="b6359-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b6359-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b6359-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b6359-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b6359-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b6359-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b6359-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b6359-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6359-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6359-126">Requirements</span></span>



| <span data-ttu-id="b6359-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6359-127">Requirement</span></span> | <span data-ttu-id="b6359-128">Value</span><span class="sxs-lookup"><span data-stu-id="b6359-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6359-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6359-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b6359-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6359-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b6359-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6359-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b6359-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6359-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b6359-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6359-133">Namespace</span></span><br/>                | <span data-ttu-id="b6359-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b6359-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b6359-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b6359-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6359-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6359-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6359-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6359-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6359-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6359-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

