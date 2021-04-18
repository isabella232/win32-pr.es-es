---
description: 'Más información sobre: método Update. SaveAndGotoBookmark'
title: Método Update. SaveAndGotoBookmark
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715289"
---
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="1b548-103">Método Update. SaveAndGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="1b548-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="1b548-104">Actualice el TABLEID y coloque el TABLEID en el registro que se modificó.</span><span class="sxs-lookup"><span data-stu-id="1b548-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="1b548-105">Esto puede ser útil al insertar un registro porque, de forma predeterminada, el TABLEID permanece en su ubicación anterior.</span><span class="sxs-lookup"><span data-stu-id="1b548-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="1b548-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1b548-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1b548-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1b548-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1b548-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b548-108">Syntax</span></span>

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a><span data-ttu-id="1b548-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b548-109">Remarks</span></span>

<span data-ttu-id="1b548-110">Guardar es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="1b548-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="1b548-111">La actualización se inicia llamando a crear un objeto Update y llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="1b548-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="1b548-112">Por último, se llama a Update para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="1b548-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="1b548-113">Los índices solo se actualizan mediante Update o y no durante JetSetColumn ni JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="1b548-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b548-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b548-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1b548-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="1b548-115">Reference</span></span>

[<span data-ttu-id="1b548-116">Update (clase)</span><span class="sxs-lookup"><span data-stu-id="1b548-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="1b548-117">Actualizar miembros</span><span class="sxs-lookup"><span data-stu-id="1b548-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="1b548-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1b548-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
