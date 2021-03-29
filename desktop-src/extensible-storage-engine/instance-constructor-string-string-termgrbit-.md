---
description: 'Más información sobre: constructor de instancia (String, String, TermGrbit)'
title: Constructor de instancia (String, String, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811126"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="34df7-103">Constructor de instancia (String, String, TermGrbit)</span><span class="sxs-lookup"><span data-stu-id="34df7-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="34df7-104">Inicializa una nueva instancia de la clase de instancia.</span><span class="sxs-lookup"><span data-stu-id="34df7-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="34df7-105">La JET_INSTANCE subyacente está asignada, pero no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="34df7-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="34df7-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34df7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34df7-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34df7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34df7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34df7-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="34df7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34df7-109">Parameters</span></span>

  - <span data-ttu-id="34df7-110">name</span><span class="sxs-lookup"><span data-stu-id="34df7-110">name</span></span>  
    <span data-ttu-id="34df7-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="34df7-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="34df7-112">Nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="34df7-112">The name of the instance.</span></span> <span data-ttu-id="34df7-113">Esta cadena debe ser única dentro de un proceso determinado que hospede el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="34df7-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="34df7-114">DisplayName</span><span class="sxs-lookup"><span data-stu-id="34df7-114">displayName</span></span>  
    <span data-ttu-id="34df7-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="34df7-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="34df7-116">Nombre para mostrar de la instancia.</span><span class="sxs-lookup"><span data-stu-id="34df7-116">A display name for the instance.</span></span> <span data-ttu-id="34df7-117">Se utilizará en las entradas del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="34df7-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="34df7-118">termGrbit</span><span class="sxs-lookup"><span data-stu-id="34df7-118">termGrbit</span></span>  
    <span data-ttu-id="34df7-119">Tipo: [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="34df7-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="34df7-120">TermGrbit que se va a usar en JetTerm Time.</span><span class="sxs-lookup"><span data-stu-id="34df7-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="34df7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="34df7-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34df7-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="34df7-122">Reference</span></span>

[<span data-ttu-id="34df7-123">Clase de instancia</span><span class="sxs-lookup"><span data-stu-id="34df7-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="34df7-124">Miembros de instancia</span><span class="sxs-lookup"><span data-stu-id="34df7-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="34df7-125">Sobrecarga de instancia</span><span class="sxs-lookup"><span data-stu-id="34df7-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="34df7-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="34df7-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
