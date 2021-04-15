---
description: 'Más información acerca de: API. GetBookmark (método)'
title: API. GetBookmark (método)
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539750"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="24679-103">API. GetBookmark (método)</span><span class="sxs-lookup"><span data-stu-id="24679-103">Api.GetBookmark method</span></span>

<span data-ttu-id="24679-104">Recupera el marcador del registro asociado a la entrada de índice en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="24679-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="24679-105">Este marcador se puede usar para volver a colocar el cursor en el mismo registro mediante JetGotoBookmark.</span><span class="sxs-lookup"><span data-stu-id="24679-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="24679-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24679-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24679-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24679-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24679-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24679-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="24679-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24679-109">Parameters</span></span>

  - <span data-ttu-id="24679-110">sesid</span><span class="sxs-lookup"><span data-stu-id="24679-110">sesid</span></span>  
    <span data-ttu-id="24679-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24679-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="24679-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="24679-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="24679-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="24679-113">tableid</span></span>  
    <span data-ttu-id="24679-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24679-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="24679-115">Cursor del que se va a recuperar el marcador.</span><span class="sxs-lookup"><span data-stu-id="24679-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="24679-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24679-116">Return value</span></span>

<span data-ttu-id="24679-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="24679-117">Type: \[\]</span></span>  
<span data-ttu-id="24679-118">Marcador del registro.</span><span class="sxs-lookup"><span data-stu-id="24679-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="24679-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="24679-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24679-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="24679-120">Reference</span></span>

[<span data-ttu-id="24679-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="24679-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="24679-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="24679-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="24679-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="24679-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
