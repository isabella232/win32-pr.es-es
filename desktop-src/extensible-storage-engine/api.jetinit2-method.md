---
description: 'Más información sobre: API. JetInit2 (método)'
title: Método API. JetInit2
TOCTitle: 'JetInit2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit2(v=EXCHG.10)
ms:contentKeyID: 55100762
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 138a9830d5a74b887e7e68f3a3833f5f7e7fb8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716755"
---
# <a name="apijetinit2-method"></a><span data-ttu-id="eb679-103">Método API. JetInit2</span><span class="sxs-lookup"><span data-stu-id="eb679-103">Api.JetInit2 method</span></span>

<span data-ttu-id="eb679-104">Inicialice el motor de base de datos ESENT.</span><span class="sxs-lookup"><span data-stu-id="eb679-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="eb679-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb679-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb679-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb679-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb679-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb679-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit2 ( _
    ByRef instance As JET_INSTANCE, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetInit2(instance, _
    grbit)
```

``` csharp
public static JET_wrn JetInit2(
    ref JET_INSTANCE instance,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="eb679-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb679-108">Parameters</span></span>

  - <span data-ttu-id="eb679-109">instance</span><span class="sxs-lookup"><span data-stu-id="eb679-109">instance</span></span>  
    <span data-ttu-id="eb679-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb679-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="eb679-111">Instancia de que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="eb679-111">The instance to initialize.</span></span> <span data-ttu-id="eb679-112">Si no se ha asignado una instancia, se crea una nueva y el motor funcionará en modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="eb679-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb679-113">grbit</span><span class="sxs-lookup"><span data-stu-id="eb679-113">grbit</span></span>  
    <span data-ttu-id="eb679-114">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="eb679-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="eb679-115">Opciones de inicialización.</span><span class="sxs-lookup"><span data-stu-id="eb679-115">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eb679-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb679-116">Return value</span></span>

<span data-ttu-id="eb679-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="eb679-117">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="eb679-118">Código de advertencia.</span><span class="sxs-lookup"><span data-stu-id="eb679-118">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb679-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb679-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb679-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="eb679-120">Reference</span></span>

[<span data-ttu-id="eb679-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="eb679-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="eb679-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="eb679-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="eb679-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eb679-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
