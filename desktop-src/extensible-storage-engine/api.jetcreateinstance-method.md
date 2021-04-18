---
description: 'Más información sobre: API. JetCreateInstance (método)'
title: Método API. JetCreateInstance
TOCTitle: 'JetCreateInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance(v=EXCHG.10)
ms:contentKeyID: 55100672
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e865c443d4f19b14a955204840355ee73be8773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715053"
---
# <a name="apijetcreateinstance-method"></a><span data-ttu-id="4b652-103">Método API. JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4b652-103">Api.JetCreateInstance method</span></span>

<span data-ttu-id="4b652-104">Asigna una nueva instancia del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4b652-104">Allocates a new instance of the database engine.</span></span>

<span data-ttu-id="4b652-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b652-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b652-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4b652-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b652-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b652-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As StringApi.JetCreateInstance(instance, _
    name)
```

``` csharp
public static void JetCreateInstance(
    out JET_INSTANCE instance,
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="4b652-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b652-108">Parameters</span></span>

  - <span data-ttu-id="4b652-109">instance</span><span class="sxs-lookup"><span data-stu-id="4b652-109">instance</span></span>  
    <span data-ttu-id="4b652-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4b652-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="4b652-111">Devuelve la nueva instancia de.</span><span class="sxs-lookup"><span data-stu-id="4b652-111">Returns the new instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="4b652-112">name</span><span class="sxs-lookup"><span data-stu-id="4b652-112">name</span></span>  
    <span data-ttu-id="4b652-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4b652-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4b652-114">Nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="4b652-114">The name of the instance.</span></span> <span data-ttu-id="4b652-115">Los nombres deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="4b652-115">Names must be unique.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b652-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b652-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b652-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="4b652-117">Reference</span></span>

[<span data-ttu-id="4b652-118">Clase de API</span><span class="sxs-lookup"><span data-stu-id="4b652-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4b652-119">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="4b652-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4b652-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4b652-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
