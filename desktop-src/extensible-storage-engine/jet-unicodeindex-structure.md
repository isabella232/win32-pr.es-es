---
description: 'Más información acerca de: estructura de JET_UNICODEINDEX'
title: Estructura de JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104424547"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="19860-103">Estructura de JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="19860-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="19860-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="19860-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="19860-105">Estructura de JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="19860-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="19860-106">La estructura **JET_UNICODEINDEX** Personaliza cómo se normalizan los datos Unicode cuando se crea un índice en una columna Unicode.</span><span class="sxs-lookup"><span data-stu-id="19860-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="19860-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="19860-107">Members</span></span>

<span data-ttu-id="19860-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="19860-108">**lcid**</span></span>

<span data-ttu-id="19860-109">IDENTIFICADOR de configuración regional que se va a usar al normalizar los datos.</span><span class="sxs-lookup"><span data-stu-id="19860-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="19860-110">Se puede usar cualquier configuración regional siempre que se haya instalado en el equipo el paquete de idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="19860-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="19860-111">La única excepción es que la configuración regional neutra de idioma (LCID de cero) no es válida.</span><span class="sxs-lookup"><span data-stu-id="19860-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="19860-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="19860-112">**dwMapFlags**</span></span>

<span data-ttu-id="19860-113">Estas marcas se pasan a [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) cuando los datos Unicode se normalizan en una clave, lo que permite que las marcas definidas por el usuario invalide el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19860-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="19860-114">**Windows 2000**: los únicos dos valores válidos para **dwFlags** son:</span><span class="sxs-lookup"><span data-stu-id="19860-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="19860-115">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)</span><span class="sxs-lookup"><span data-stu-id="19860-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="19860-116">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)</span><span class="sxs-lookup"><span data-stu-id="19860-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="19860-117">**dwMapFlags** tiene las siguientes restricciones.</span><span class="sxs-lookup"><span data-stu-id="19860-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19860-118">Value</span><span class="sxs-lookup"><span data-stu-id="19860-118">Value</span></span></p></th>
<th><p><span data-ttu-id="19860-119">Significado</span><span class="sxs-lookup"><span data-stu-id="19860-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19860-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="19860-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="19860-121">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="19860-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19860-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="19860-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="19860-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19860-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="19860-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="19860-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19860-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="19860-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="19860-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19860-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="19860-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="19860-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19860-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="19860-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="19860-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19860-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="19860-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="19860-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19860-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="19860-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="19860-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19860-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="19860-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19860-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19860-137"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="19860-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="19860-138">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="19860-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19860-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="19860-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="19860-140">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="19860-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19860-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="19860-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="19860-142">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="19860-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="19860-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="19860-143">See Also</span></span>

[<span data-ttu-id="19860-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="19860-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="19860-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="19860-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="19860-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="19860-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
