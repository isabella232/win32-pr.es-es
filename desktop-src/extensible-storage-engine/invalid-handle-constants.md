---
description: 'Más información sobre: constantes de identificador no válidas'
title: Constantes de identificador no válidas
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083278"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="a4884-103">Constantes de identificador no válidas</span><span class="sxs-lookup"><span data-stu-id="a4884-103">Invalid Handle Constants</span></span>


<span data-ttu-id="a4884-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a4884-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="a4884-105">Constantes de identificador no válidas</span><span class="sxs-lookup"><span data-stu-id="a4884-105">Invalid Handle Constants</span></span>

<span data-ttu-id="a4884-106">Las constantes siguientes indican controladores no válidos para distintos aspectos de ESE.</span><span class="sxs-lookup"><span data-stu-id="a4884-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4884-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a4884-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="a4884-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4884-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4884-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="a4884-109">JET_instanceNil</span></span><br />
<span data-ttu-id="a4884-110">(~ (JET_INSTANCE) 0)</span><span class="sxs-lookup"><span data-stu-id="a4884-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="a4884-111">Identificador no válido para una instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4884-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="a4884-112">
<strong>Windows XP:</strong> Introducido en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4884-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4884-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="a4884-113">JET_sesidNil</span></span><br />
<span data-ttu-id="a4884-114">(~ (JET_SESID) 0)</span><span class="sxs-lookup"><span data-stu-id="a4884-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="a4884-115">Identificador no válido para un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="a4884-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4884-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="a4884-116">JET_tableidNil</span></span><br />
<span data-ttu-id="a4884-117">(~ (JET_TABLEID) 0)</span><span class="sxs-lookup"><span data-stu-id="a4884-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="a4884-118">Identificador no válido para un ID. de tabla.</span><span class="sxs-lookup"><span data-stu-id="a4884-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4884-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="a4884-119">JET_bitNil</span></span><br />
<span data-ttu-id="a4884-120">((JET_GRBIT) 0)</span><span class="sxs-lookup"><span data-stu-id="a4884-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="a4884-121">Identificador no válido para un grupo de bits.</span><span class="sxs-lookup"><span data-stu-id="a4884-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4884-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="a4884-122">JET_LSNil</span></span><br />
<span data-ttu-id="a4884-123">(~ (JET_LS) 0)</span><span class="sxs-lookup"><span data-stu-id="a4884-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="a4884-124">Identificador no válido para el almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="a4884-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4884-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="a4884-125">JET_dbidNil</span></span><br />
<span data-ttu-id="a4884-126">((JET_DBID) 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="a4884-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="a4884-127">Identificador no válido para el identificador de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4884-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a4884-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4884-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4884-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a4884-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a4884-130">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a4884-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4884-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a4884-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a4884-132">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a4884-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4884-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a4884-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a4884-134">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a4884-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

