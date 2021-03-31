---
title: Win32_TSVirtualDesktopServerSettings (clase)
description: Contiene información de configuración para un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSVirtualDesktopServerSettings de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803601"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="7559a-105">\_Clase Win32 TSVirtualDesktopServerSettings</span><span class="sxs-lookup"><span data-stu-id="7559a-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="7559a-106">Contiene información de configuración para un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="7559a-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="7559a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7559a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7559a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7559a-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="7559a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7559a-109">Members</span></span>

<span data-ttu-id="7559a-110">La **clase \_ TSVirtualDesktopServerSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7559a-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="7559a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7559a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7559a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7559a-112">Properties</span></span>

<span data-ttu-id="7559a-113">La **clase \_ TSVirtualDesktopServerSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7559a-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7559a-114">**Simultaneidad**</span><span class="sxs-lookup"><span data-stu-id="7559a-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7559a-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7559a-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7559a-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7559a-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7559a-117">Número máximo de solicitudes de aprovisionamiento simultáneas permitidas para este servidor de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="7559a-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="7559a-118">**PolicySourceSessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="7559a-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7559a-119">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7559a-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7559a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7559a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7559a-121">Si se establece en 0, indica que el servidor configura la propiedad **SessionBrokerName** ; Si se establece en 1, indica que la propiedad **SessionBrokerName** está configurada por una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="7559a-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="7559a-122">**SessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="7559a-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7559a-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7559a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7559a-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7559a-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7559a-125">Nombre distintivo completo del agente de sesiones para el servidor host de virtualización de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="7559a-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7559a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7559a-126">Requirements</span></span>



| <span data-ttu-id="7559a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7559a-127">Requirement</span></span> | <span data-ttu-id="7559a-128">Value</span><span class="sxs-lookup"><span data-stu-id="7559a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7559a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7559a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7559a-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7559a-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="7559a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7559a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7559a-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7559a-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="7559a-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7559a-133">Namespace</span></span><br/>                | <span data-ttu-id="7559a-134">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7559a-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="7559a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7559a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7559a-136"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7559a-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="7559a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7559a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7559a-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7559a-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





