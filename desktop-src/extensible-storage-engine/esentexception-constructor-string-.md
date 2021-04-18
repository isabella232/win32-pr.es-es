---
description: 'Más información sobre: constructor EsentException (String)'
title: Constructor EsentException (String) (Microsoft. ISAM. esent)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707246"
---
# <a name="esentexception-constructor-string"></a><span data-ttu-id="44bf1-103">Constructor EsentException (String)</span><span class="sxs-lookup"><span data-stu-id="44bf1-103">EsentException constructor (String)</span></span>

<span data-ttu-id="44bf1-104">Inicializa una nueva instancia de la clase EsentException con un mensaje de error especificado.</span><span class="sxs-lookup"><span data-stu-id="44bf1-104">Initializes a new instance of the EsentException class with a specified error message.</span></span>

<span data-ttu-id="44bf1-105">**Espacio de nombres:**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44bf1-105">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="44bf1-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44bf1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44bf1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44bf1-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a><span data-ttu-id="44bf1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44bf1-108">Parameters</span></span>

  - <span data-ttu-id="44bf1-109">message</span><span class="sxs-lookup"><span data-stu-id="44bf1-109">message</span></span>  
    <span data-ttu-id="44bf1-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="44bf1-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="44bf1-111">Mensaje que describe el error.</span><span class="sxs-lookup"><span data-stu-id="44bf1-111">The message that describes the error.</span></span>

## <a name="see-also"></a><span data-ttu-id="44bf1-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="44bf1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44bf1-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="44bf1-113">Reference</span></span>

[<span data-ttu-id="44bf1-114">Clase EsentException</span><span class="sxs-lookup"><span data-stu-id="44bf1-114">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="44bf1-115">Miembros de EsentException</span><span class="sxs-lookup"><span data-stu-id="44bf1-115">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="44bf1-116">Sobrecarga EsentException</span><span class="sxs-lookup"><span data-stu-id="44bf1-116">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="44bf1-117">Espacio de nombres Microsoft. ISAM. esent</span><span class="sxs-lookup"><span data-stu-id="44bf1-117">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
