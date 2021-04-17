---
description: 'Más información acerca de: JET_PFNSTATUS delegado'
title: JET_PFNSTATUS delegado
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697455"
---
# <a name="jet_pfnstatus-delegate"></a><span data-ttu-id="cbd38-103">JET_PFNSTATUS delegado</span><span class="sxs-lookup"><span data-stu-id="cbd38-103">JET_PFNSTATUS delegate</span></span>

<span data-ttu-id="cbd38-104">Recibe información sobre el progreso de las operaciones de ejecución prolongada, como la desfragmentación, la copia de seguridad o las operaciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="cbd38-104">Receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="cbd38-105">Durante estas operaciones, el motor de base de datos llama a esta función de devolución de llamada para proporcionar una actualización en el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="cbd38-105">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

<span data-ttu-id="cbd38-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cbd38-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cbd38-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cbd38-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd38-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbd38-108">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a><span data-ttu-id="cbd38-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbd38-109">Parameters</span></span>

  - <span data-ttu-id="cbd38-110">sesid</span><span class="sxs-lookup"><span data-stu-id="cbd38-110">sesid</span></span>  
    <span data-ttu-id="cbd38-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cbd38-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cbd38-112">La sesión con la que se llamó a la operación de larga ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbd38-112">The session with which the long running operation was called.</span></span>

<!-- end list -->

  - <span data-ttu-id="cbd38-113">SNP</span><span class="sxs-lookup"><span data-stu-id="cbd38-113">snp</span></span>  
    <span data-ttu-id="cbd38-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cbd38-114">Type: [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span></span>  
    
    <span data-ttu-id="cbd38-115">Tipo de operación.</span><span class="sxs-lookup"><span data-stu-id="cbd38-115">The type of operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="cbd38-116">SNT</span><span class="sxs-lookup"><span data-stu-id="cbd38-116">snt</span></span>  
    <span data-ttu-id="cbd38-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cbd38-117">Type: [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span></span>  
    
    <span data-ttu-id="cbd38-118">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="cbd38-118">The status of the operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="cbd38-119">datos</span><span class="sxs-lookup"><span data-stu-id="cbd38-119">data</span></span>  
    <span data-ttu-id="cbd38-120">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="cbd38-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="cbd38-121">Datos opcionales.</span><span class="sxs-lookup"><span data-stu-id="cbd38-121">Optional data.</span></span> <span data-ttu-id="cbd38-122">Puede ser un [JET_SNPROG](./jet-snprog-class.md).</span><span class="sxs-lookup"><span data-stu-id="cbd38-122">May be a [JET_SNPROG](./jet-snprog-class.md).</span></span>

#### <a name="return-value"></a><span data-ttu-id="cbd38-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbd38-123">Return value</span></span>

<span data-ttu-id="cbd38-124">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cbd38-124">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="cbd38-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbd38-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbd38-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="cbd38-126">Reference</span></span>

[<span data-ttu-id="cbd38-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cbd38-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
