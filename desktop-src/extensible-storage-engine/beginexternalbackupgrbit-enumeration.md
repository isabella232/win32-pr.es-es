---
description: 'Más información sobre: enumeración BeginExternalBackupGrbit'
title: Enumeración BeginExternalBackupGrbit
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678415"
---
# <a name="beginexternalbackupgrbit-enumeration"></a><span data-ttu-id="026ee-103">Enumeración BeginExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="026ee-103">BeginExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="026ee-104">Opciones de [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="026ee-104">Options for [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="026ee-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="026ee-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="026ee-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="026ee-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="026ee-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="026ee-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="026ee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="026ee-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="026ee-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="026ee-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="026ee-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="026ee-110">Member name</span></span></th>
<th><span data-ttu-id="026ee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="026ee-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="026ee-112">None</span><span class="sxs-lookup"><span data-stu-id="026ee-112">None</span></span></td>
<td><span data-ttu-id="026ee-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="026ee-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="026ee-114">Incremental</span><span class="sxs-lookup"><span data-stu-id="026ee-114">Incremental</span></span></td>
<td><span data-ttu-id="026ee-115">Crea una copia de seguridad incremental en lugar de una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="026ee-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="026ee-116">Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="026ee-116">This means that only the log files since the last full or incremental backup will be backed up.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="026ee-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="026ee-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="026ee-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="026ee-118">Reference</span></span>

[<span data-ttu-id="026ee-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="026ee-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
