---
title: MSAD_NamingContext (clase)
description: Representa un contexto de nomenclatura determinado (NC) en el controlador de dominio.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingContext clase Active Directory
- Active Directory de MSAD_NamingContext de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802341"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="e46b5-105">MSAD \_ NamingContext (clase)</span><span class="sxs-lookup"><span data-stu-id="e46b5-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="e46b5-106">Representa un contexto de nomenclatura determinado (NC) en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="e46b5-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e46b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e46b5-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="e46b5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e46b5-108">Members</span></span>

<span data-ttu-id="e46b5-109">La clase **MSAD \_ NamingContext** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e46b5-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="e46b5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e46b5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e46b5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e46b5-111">Properties</span></span>

<span data-ttu-id="e46b5-112">La clase **MSAD \_ NamingContext** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e46b5-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e46b5-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="e46b5-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e46b5-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e46b5-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="e46b5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e46b5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e46b5-116">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e46b5-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e46b5-117">Obtiene la ruta de acceso X. 500 de la NC.</span><span class="sxs-lookup"><span data-stu-id="e46b5-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="e46b5-118">**IsFullReplica**</span><span class="sxs-lookup"><span data-stu-id="e46b5-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e46b5-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e46b5-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e46b5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e46b5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e46b5-121">Obtiene el valor que indica si el NC es de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="e46b5-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="e46b5-122">**True** si el NC es de lectura/escritura; **False** si el NC es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e46b5-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e46b5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e46b5-123">Requirements</span></span>



| <span data-ttu-id="e46b5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e46b5-124">Requirement</span></span> | <span data-ttu-id="e46b5-125">Value</span><span class="sxs-lookup"><span data-stu-id="e46b5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e46b5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e46b5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e46b5-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e46b5-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e46b5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e46b5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e46b5-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e46b5-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e46b5-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e46b5-130">Namespace</span></span><br/>                | <span data-ttu-id="e46b5-131">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="e46b5-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="e46b5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e46b5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e46b5-133"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e46b5-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="e46b5-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e46b5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e46b5-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e46b5-135"><dt>Replprov.dll</dt></span></span> </dl> |



 

