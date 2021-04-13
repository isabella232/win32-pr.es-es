---
description: 'Más información sobre: parámetros del sistema del motor de almacenamiento extensible'
title: Parámetros del sistema del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
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
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544011"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="06614-103">Parámetros del sistema del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="06614-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="06614-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06614-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="06614-105">Parámetros del sistema del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="06614-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="06614-106">Las constantes siguientes se usan como valores para el parámetro *paramid* de las funciones [JetGetSystemParameter](./jetgetsystemparameter-function.md) y [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="06614-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="06614-107">Parámetros de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="06614-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="06614-108">Parámetros de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="06614-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="06614-109">Parámetros de base de datos</span><span class="sxs-lookup"><span data-stu-id="06614-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="06614-110">Parámetros de caché de base de datos</span><span class="sxs-lookup"><span data-stu-id="06614-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="06614-111">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="06614-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="06614-112">Parámetros del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="06614-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="06614-113">Parámetros de e/s</span><span class="sxs-lookup"><span data-stu-id="06614-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="06614-114">Parámetros de índice</span><span class="sxs-lookup"><span data-stu-id="06614-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="06614-115">Parámetros informativos</span><span class="sxs-lookup"><span data-stu-id="06614-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="06614-116">Metaparámetros</span><span class="sxs-lookup"><span data-stu-id="06614-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="06614-117">Parámetros de recursos</span><span class="sxs-lookup"><span data-stu-id="06614-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="06614-118">Parámetros temporales de base de datos</span><span class="sxs-lookup"><span data-stu-id="06614-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="06614-119">Parámetros de registro de transacciones</span><span class="sxs-lookup"><span data-stu-id="06614-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="06614-120">Formato de descripción de parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="06614-120">System Parameter Description Format</span></span>

<span data-ttu-id="06614-121">Cada parámetro del sistema se describe con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="06614-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="06614-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="06614-122">JET_paramX</span></span>

<span data-ttu-id="06614-123">Descripción del parámetro del sistema JET_paramX.</span><span class="sxs-lookup"><span data-stu-id="06614-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06614-124">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="06614-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="06614-125">Valor predeterminado del parámetro.</span><span class="sxs-lookup"><span data-stu-id="06614-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06614-126">Escriba:</span><span class="sxs-lookup"><span data-stu-id="06614-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="06614-127">El tipo de datos del parámetro.</span><span class="sxs-lookup"><span data-stu-id="06614-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06614-128">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="06614-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="06614-129">Valores válidos para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="06614-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06614-130">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="06614-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="06614-131">¿El parámetro es global o por instancia?</span><span class="sxs-lookup"><span data-stu-id="06614-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06614-132">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="06614-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="06614-133">¿Se puede establecer el parámetro si existe alguna instancia?</span><span class="sxs-lookup"><span data-stu-id="06614-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06614-134">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="06614-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="06614-135">¿Se puede establecer el parámetro al inicializarse?</span><span class="sxs-lookup"><span data-stu-id="06614-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06614-136">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="06614-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="06614-137">¿El parámetro afecta a los archivos en el disco?</span><span class="sxs-lookup"><span data-stu-id="06614-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06614-138">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="06614-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="06614-139">¿Afecta el parámetro a la confiabilidad del motor?</span><span class="sxs-lookup"><span data-stu-id="06614-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06614-140">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="06614-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="06614-141">¿Afecta el parámetro al rendimiento del motor?</span><span class="sxs-lookup"><span data-stu-id="06614-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06614-142">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="06614-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="06614-143">¿Afecta el parámetro a los recursos del motor?</span><span class="sxs-lookup"><span data-stu-id="06614-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06614-144">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="06614-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="06614-145">Versiones de Windows que admiten el parámetro.</span><span class="sxs-lookup"><span data-stu-id="06614-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
