---
description: 'Más información sobre: método Update. Save'
title: Update. Save (método)
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389034"
---
# <a name="updatesave-method"></a><span data-ttu-id="c5328-103">Update. Save (método)</span><span class="sxs-lookup"><span data-stu-id="c5328-103">Update.Save method</span></span>

<span data-ttu-id="c5328-104">Actualice el ID. de la.</span><span class="sxs-lookup"><span data-stu-id="c5328-104">Update the tableid.</span></span>

<span data-ttu-id="c5328-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5328-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5328-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c5328-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5328-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5328-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="c5328-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5328-108">Remarks</span></span>

<span data-ttu-id="c5328-109">Guardar es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="c5328-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="c5328-110">La actualización se inicia llamando a crear un objeto Update y llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="c5328-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="c5328-111">Por último, se llama a Update para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="c5328-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="c5328-112">Los índices solo se actualizan mediante Update o y no durante JetSetColumn ni JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="c5328-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5328-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5328-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5328-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="c5328-114">Reference</span></span>

[<span data-ttu-id="c5328-115">Update (clase)</span><span class="sxs-lookup"><span data-stu-id="c5328-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="c5328-116">Actualizar miembros</span><span class="sxs-lookup"><span data-stu-id="c5328-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="c5328-117">Guardar sobrecarga</span><span class="sxs-lookup"><span data-stu-id="c5328-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="c5328-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c5328-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
