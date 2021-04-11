---
title: Win32_SessionDirectoryVirtualDesktopServer (clase)
description: Representa un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto) unido a un agente de sesión.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryVirtualDesktopServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079090"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="cb21f-105">\_Clase Win32 SessionDirectoryVirtualDesktopServer</span><span class="sxs-lookup"><span data-stu-id="cb21f-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="cb21f-106">Representa un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto) unido a un agente de sesión.</span><span class="sxs-lookup"><span data-stu-id="cb21f-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="cb21f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cb21f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb21f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb21f-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="cb21f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb21f-109">Members</span></span>

<span data-ttu-id="cb21f-110">La **clase \_ SessionDirectoryVirtualDesktopServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb21f-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="cb21f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb21f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb21f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb21f-112">Properties</span></span>

<span data-ttu-id="cb21f-113">La **clase \_ SessionDirectoryVirtualDesktopServer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb21f-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb21f-114">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="cb21f-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb21f-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cb21f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb21f-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb21f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb21f-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb21f-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cb21f-118">Nombre DNS del servidor host de virtualización de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cb21f-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="cb21f-119">Este nombre tiene el formato "*MachineName*. *Dominio*. com ".</span><span class="sxs-lookup"><span data-stu-id="cb21f-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb21f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb21f-120">Requirements</span></span>



| <span data-ttu-id="cb21f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb21f-121">Requirement</span></span> | <span data-ttu-id="cb21f-122">Value</span><span class="sxs-lookup"><span data-stu-id="cb21f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb21f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb21f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cb21f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb21f-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cb21f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb21f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cb21f-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb21f-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="cb21f-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb21f-127">Namespace</span></span><br/>                | <span data-ttu-id="cb21f-128">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cb21f-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="cb21f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="cb21f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb21f-130"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb21f-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb21f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb21f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb21f-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb21f-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

