---
description: 'Más información sobre: API. JetRollback (método)'
title: Método API. JetRollback
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9144bade272ddaea7501be5622c7263268c0f1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360210"
---
# <a name="apijetrollback-method"></a><span data-ttu-id="89280-103">Método API. JetRollback</span><span class="sxs-lookup"><span data-stu-id="89280-103">Api.JetRollback method</span></span>

<span data-ttu-id="89280-104">Deshace los cambios realizados en el estado de la base de datos y vuelve al último punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="89280-104">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="89280-105">JetRollback también cerrará los cursores abiertos durante el punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="89280-105">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="89280-106">Si el punto de almacenamiento más externo se deshace, la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="89280-106">If the outermost save point is undone, the session will exit the transaction.</span></span>

<span data-ttu-id="89280-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89280-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89280-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89280-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89280-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89280-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="89280-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89280-110">Parameters</span></span>

  - <span data-ttu-id="89280-111">sesid</span><span class="sxs-lookup"><span data-stu-id="89280-111">sesid</span></span>  
    <span data-ttu-id="89280-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89280-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="89280-113">Sesión para la que se va a revertir la transacción.</span><span class="sxs-lookup"><span data-stu-id="89280-113">The session to rollback the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="89280-114">grbit</span><span class="sxs-lookup"><span data-stu-id="89280-114">grbit</span></span>  
    <span data-ttu-id="89280-115">Tipo: [Microsoft. ISAM. esent. Interop. RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="89280-115">Type: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="89280-116">Opciones de reversión.</span><span class="sxs-lookup"><span data-stu-id="89280-116">Rollback options.</span></span>

## <a name="see-also"></a><span data-ttu-id="89280-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="89280-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89280-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="89280-118">Reference</span></span>

[<span data-ttu-id="89280-119">Clase de API</span><span class="sxs-lookup"><span data-stu-id="89280-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="89280-120">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="89280-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="89280-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89280-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
