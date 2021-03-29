---
description: 'Más información sobre: API. RetrieveKey (método)'
title: Método API. RetrieveKey
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcabab7639a9cf3128b0b2c314ba60c2de8f8e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808269"
---
# <a name="apiretrievekey-method"></a><span data-ttu-id="437e1-103">Método API. RetrieveKey</span><span class="sxs-lookup"><span data-stu-id="437e1-103">Api.RetrieveKey method</span></span>

<span data-ttu-id="437e1-104">Recupera la clave de la entrada de índice en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="437e1-104">Retrieves the key for the index entry at the current position of a cursor.</span></span>

<span data-ttu-id="437e1-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="437e1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="437e1-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="437e1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="437e1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="437e1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="437e1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="437e1-108">Parameters</span></span>

  - <span data-ttu-id="437e1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="437e1-109">sesid</span></span>  
    <span data-ttu-id="437e1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="437e1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="437e1-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="437e1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="437e1-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="437e1-112">tableid</span></span>  
    <span data-ttu-id="437e1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="437e1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="437e1-114">Cursor del que se va a recuperar la clave.</span><span class="sxs-lookup"><span data-stu-id="437e1-114">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="437e1-115">grbit</span><span class="sxs-lookup"><span data-stu-id="437e1-115">grbit</span></span>  
    <span data-ttu-id="437e1-116">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="437e1-116">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="437e1-117">Recupera las opciones de clave.</span><span class="sxs-lookup"><span data-stu-id="437e1-117">Retrieve key options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="437e1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="437e1-118">Return value</span></span>

<span data-ttu-id="437e1-119">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="437e1-119">Type: \[\]</span></span>  
<span data-ttu-id="437e1-120">La clave recuperada.</span><span class="sxs-lookup"><span data-stu-id="437e1-120">The retrieved key.</span></span>  

## <a name="see-also"></a><span data-ttu-id="437e1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="437e1-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="437e1-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="437e1-122">Reference</span></span>

[<span data-ttu-id="437e1-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="437e1-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="437e1-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="437e1-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="437e1-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="437e1-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
