---
description: 'Más información sobre: constructor de instancia (String, String)'
title: Constructor de instancia (String, String)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360445"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="2ea5f-103">Constructor de instancia (String, String)</span><span class="sxs-lookup"><span data-stu-id="2ea5f-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="2ea5f-104">Inicializa una nueva instancia de la clase de instancia.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="2ea5f-105">La JET_INSTANCE subyacente está asignada, pero no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="2ea5f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ea5f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ea5f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2ea5f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea5f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ea5f-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="2ea5f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ea5f-109">Parameters</span></span>

  - <span data-ttu-id="2ea5f-110">name</span><span class="sxs-lookup"><span data-stu-id="2ea5f-110">name</span></span>  
    <span data-ttu-id="2ea5f-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2ea5f-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2ea5f-112">Nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-112">The name of the instance.</span></span> <span data-ttu-id="2ea5f-113">Esta cadena debe ser única dentro de un proceso determinado que hospede el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="2ea5f-114">DisplayName</span><span class="sxs-lookup"><span data-stu-id="2ea5f-114">displayName</span></span>  
    <span data-ttu-id="2ea5f-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2ea5f-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2ea5f-116">Nombre para mostrar de la instancia.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-116">A display name for the instance.</span></span> <span data-ttu-id="2ea5f-117">Se utilizará en las entradas del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ea5f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ea5f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ea5f-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="2ea5f-119">Reference</span></span>

[<span data-ttu-id="2ea5f-120">Clase de instancia</span><span class="sxs-lookup"><span data-stu-id="2ea5f-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="2ea5f-121">Miembros de instancia</span><span class="sxs-lookup"><span data-stu-id="2ea5f-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="2ea5f-122">Sobrecarga de instancia</span><span class="sxs-lookup"><span data-stu-id="2ea5f-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="2ea5f-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2ea5f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
