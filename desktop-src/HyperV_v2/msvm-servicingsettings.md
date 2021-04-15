---
description: Contiene los valores utilizados durante las operaciones de mantenimiento.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Msvm_ServicingSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497705"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="9f4b5-103">MSVM \_ ServicingSettings (clase)</span><span class="sxs-lookup"><span data-stu-id="9f4b5-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="9f4b5-104">Contiene los valores utilizados durante las operaciones de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="9f4b5-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="9f4b5-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9f4b5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4b5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f4b5-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="9f4b5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f4b5-107">Members</span></span>

<span data-ttu-id="9f4b5-108">La clase **MSVM \_ ServicingSettings** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f4b5-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="9f4b5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4b5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f4b5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4b5-110">Properties</span></span>

<span data-ttu-id="9f4b5-111">La clase **MSVM \_ ServicingSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f4b5-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f4b5-112">**Versión**</span><span class="sxs-lookup"><span data-stu-id="9f4b5-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4b5-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9f4b5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f4b5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4b5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4b5-115">Contiene la versión de la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="9f4b5-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f4b5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f4b5-116">Requirements</span></span>



| <span data-ttu-id="9f4b5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f4b5-117">Requirement</span></span> | <span data-ttu-id="9f4b5-118">Value</span><span class="sxs-lookup"><span data-stu-id="9f4b5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4b5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f4b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f4b5-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f4b5-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9f4b5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f4b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f4b5-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f4b5-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f4b5-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f4b5-123">Namespace</span></span><br/>                | <span data-ttu-id="9f4b5-124">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9f4b5-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f4b5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="9f4b5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f4b5-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f4b5-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f4b5-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f4b5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f4b5-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f4b5-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




