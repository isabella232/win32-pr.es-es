---
description: 'Más información sobre: enumeración CreateDatabaseGrbit'
title: Enumeración CreateDatabaseGrbit
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082248"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="61a00-103">Enumeración CreateDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="61a00-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="61a00-104">Opciones para [JetCreateDatabase (JET_SESID, cadena, cadena, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="61a00-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="61a00-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="61a00-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="61a00-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61a00-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61a00-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61a00-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61a00-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61a00-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="61a00-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="61a00-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="61a00-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="61a00-110">Member name</span></span></th>
<th><span data-ttu-id="61a00-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a00-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="61a00-112">None</span><span class="sxs-lookup"><span data-stu-id="61a00-112">None</span></span></td>
<td><span data-ttu-id="61a00-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="61a00-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="61a00-114">OverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="61a00-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="61a00-115">De forma predeterminada, si se llama a JetCreateDatabase y la base de datos ya existe, se producirá un error en la llamada a la API y no se sobrescribirá la base de datos original.</span><span class="sxs-lookup"><span data-stu-id="61a00-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="61a00-116">OverwriteExisting cambia este comportamiento y la antigua base de datos se sobrescribirá con otra nueva.</span><span class="sxs-lookup"><span data-stu-id="61a00-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="61a00-117">RecoveryOff</span><span class="sxs-lookup"><span data-stu-id="61a00-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="61a00-118">Desactiva el registro.</span><span class="sxs-lookup"><span data-stu-id="61a00-118">Turns off logging.</span></span> <span data-ttu-id="61a00-119">La configuración de este bit pierde la capacidad de reproducir archivos de registro y de recuperar la base de datos a un estado utilizable coherente después de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="61a00-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="61a00-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="61a00-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61a00-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="61a00-121">Reference</span></span>

[<span data-ttu-id="61a00-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="61a00-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
