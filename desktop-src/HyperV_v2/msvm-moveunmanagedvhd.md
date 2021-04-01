---
description: Mueve una unidad de disco duro virtual desde el origen a la ruta de acceso de destino.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Msvm_MoveUnmanagedVhd (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913117"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="9212b-103">MSVM \_ MoveUnmanagedVhd (clase)</span><span class="sxs-lookup"><span data-stu-id="9212b-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="9212b-104">Mueve una unidad de disco duro virtual desde el origen a la ruta de acceso de destino.</span><span class="sxs-lookup"><span data-stu-id="9212b-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="9212b-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9212b-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9212b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9212b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="9212b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9212b-107">Members</span></span>

<span data-ttu-id="9212b-108">La clase **MSVM \_ MoveUnmanagedVhd** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9212b-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="9212b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9212b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9212b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9212b-110">Properties</span></span>

<span data-ttu-id="9212b-111">La clase **MSVM \_ MoveUnmanagedVhd** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9212b-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9212b-112">**VhdDestinationPath**</span><span class="sxs-lookup"><span data-stu-id="9212b-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9212b-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9212b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9212b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9212b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9212b-115">La ruta de acceso de destino.</span><span class="sxs-lookup"><span data-stu-id="9212b-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="9212b-116">**VhdSourcePath**</span><span class="sxs-lookup"><span data-stu-id="9212b-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9212b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9212b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9212b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9212b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9212b-119">Ruta de acceso de origen del disco duro virtual que se va a trasladar.</span><span class="sxs-lookup"><span data-stu-id="9212b-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9212b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9212b-120">Requirements</span></span>



| <span data-ttu-id="9212b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9212b-121">Requirement</span></span> | <span data-ttu-id="9212b-122">Value</span><span class="sxs-lookup"><span data-stu-id="9212b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9212b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9212b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9212b-124">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9212b-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9212b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9212b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9212b-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9212b-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9212b-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9212b-127">Namespace</span></span><br/>                | <span data-ttu-id="9212b-128">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9212b-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9212b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9212b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9212b-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9212b-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9212b-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9212b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9212b-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9212b-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9212b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9212b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9212b-134">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9212b-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




