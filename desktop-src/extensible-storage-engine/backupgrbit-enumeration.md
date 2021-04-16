---
description: 'Más información sobre: enumeración BackupGrbit'
title: Enumeración BackupGrbit
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678417"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="9af75-103">Enumeración BackupGrbit</span><span class="sxs-lookup"><span data-stu-id="9af75-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="9af75-104">Opciones para [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="9af75-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="9af75-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="9af75-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9af75-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9af75-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9af75-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9af75-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9af75-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9af75-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="9af75-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9af75-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9af75-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="9af75-110">Member name</span></span></th>
<th><span data-ttu-id="9af75-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9af75-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9af75-112">None</span><span class="sxs-lookup"><span data-stu-id="9af75-112">None</span></span></td>
<td><span data-ttu-id="9af75-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="9af75-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9af75-114">Incremental</span><span class="sxs-lookup"><span data-stu-id="9af75-114">Incremental</span></span></td>
<td><span data-ttu-id="9af75-115">Crea una copia de seguridad incremental en lugar de una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="9af75-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="9af75-116">Esto significa que solo se realizará una copia de seguridad de los archivos de registro creados desde la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="9af75-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9af75-117">Atómico</span><span class="sxs-lookup"><span data-stu-id="9af75-117">Atomic</span></span></td>
<td><span data-ttu-id="9af75-118">Crea una copia de seguridad completa de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9af75-118">Creates a full backup of the database.</span></span> <span data-ttu-id="9af75-119">Esto permite conservar una copia de seguridad existente en el mismo directorio si se produce un error en la nueva copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9af75-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9af75-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9af75-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9af75-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="9af75-121">Reference</span></span>

[<span data-ttu-id="9af75-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9af75-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
