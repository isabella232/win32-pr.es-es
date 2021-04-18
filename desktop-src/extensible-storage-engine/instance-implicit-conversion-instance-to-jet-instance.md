---
description: Más información acerca de la conversión implícita de instancias (instancia a JET_INSTANCE)
title: Conversión implícita de instancia (instancia a JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720452"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a><span data-ttu-id="71da0-103">Conversión implícita de instancia (instancia a JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="71da0-103">Instance Implicit conversion (Instance to JET_INSTANCE)</span></span>

<span data-ttu-id="71da0-104">Proporcionar la conversión implícita de un objeto de instancia a una estructura de JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="71da0-104">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="71da0-105">Esto se hace para que se pueda usar una instancia en cualquier lugar en el que se requiera JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="71da0-105">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span>

<span data-ttu-id="71da0-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71da0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71da0-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71da0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71da0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71da0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a><span data-ttu-id="71da0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71da0-109">Parameters</span></span>

  - <span data-ttu-id="71da0-110">instance</span><span class="sxs-lookup"><span data-stu-id="71da0-110">instance</span></span>  
    <span data-ttu-id="71da0-111">Tipo: [Microsoft. ISAM. esent. Interop. Instance](./instance-class.md)</span><span class="sxs-lookup"><span data-stu-id="71da0-111">Type: [Microsoft.Isam.Esent.Interop.Instance](./instance-class.md)</span></span>  
    
    <span data-ttu-id="71da0-112">La instancia de que se convertirá.</span><span class="sxs-lookup"><span data-stu-id="71da0-112">The instance to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="71da0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71da0-113">Return value</span></span>

<span data-ttu-id="71da0-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="71da0-114">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
<span data-ttu-id="71da0-115">JET_INSTANCE encapsulado por la instancia de.</span><span class="sxs-lookup"><span data-stu-id="71da0-115">The JET_INSTANCE wrapped by the instance.</span></span>  

## <a name="see-also"></a><span data-ttu-id="71da0-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="71da0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71da0-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="71da0-117">Reference</span></span>

[<span data-ttu-id="71da0-118">Clase de instancia</span><span class="sxs-lookup"><span data-stu-id="71da0-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="71da0-119">Miembros de instancia</span><span class="sxs-lookup"><span data-stu-id="71da0-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="71da0-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="71da0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
