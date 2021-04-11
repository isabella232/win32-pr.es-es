---
title: EDB_RSTMAP estructura (Ntdsbcli. h)
description: Se usa con la función DsRestoreRegister para asignar una base de datos de copia de seguridad a una nueva base de datos.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- Estructura de EDB_RSTMAP Active Directory
- PEDB_RSTMAP puntero de estructura Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079489"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="0c3ea-105">\_Estructura RSTMAP de edb</span><span class="sxs-lookup"><span data-stu-id="0c3ea-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="0c3ea-106">La estructura **EDB \_ RSTMAP** se usa con la función [**DsRestoreRegister**](dsrestoreregister.md) para asignar una base de datos de copia de seguridad a una nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="0c3ea-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3ea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c3ea-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="0c3ea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c3ea-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c3ea-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="0c3ea-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="0c3ea-110">Puntero a una cadena terminada en null que contiene el nombre de la base de datos cuando se hizo la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0c3ea-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="0c3ea-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="0c3ea-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="0c3ea-112">Puntero a una cadena terminada en null que contiene el nuevo nombre de la base de datos, incluida su nueva ubicación, cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="0c3ea-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c3ea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c3ea-113">Requirements</span></span>



| <span data-ttu-id="0c3ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c3ea-114">Requirement</span></span> | <span data-ttu-id="0c3ea-115">Value</span><span class="sxs-lookup"><span data-stu-id="0c3ea-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3ea-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c3ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3ea-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c3ea-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="0c3ea-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c3ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3ea-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c3ea-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="0c3ea-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c3ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c3ea-121"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c3ea-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="0c3ea-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0c3ea-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0c3ea-123">**EDB \_ RSTMAPW** (Unicode) y **EDB \_ RSTMAPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0c3ea-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="0c3ea-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c3ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3ea-125">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="0c3ea-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="0c3ea-126">Estructuras de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="0c3ea-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





