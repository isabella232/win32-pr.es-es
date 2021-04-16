---
description: 'Más información acerca de: JET_CALLBACK delegado'
title: JET_CALLBACK delegado
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678326"
---
# <a name="jet_callback-delegate"></a><span data-ttu-id="325cf-103">JET_CALLBACK delegado</span><span class="sxs-lookup"><span data-stu-id="325cf-103">JET_CALLBACK delegate</span></span>

<span data-ttu-id="325cf-104">Función de devolución de llamada de varios propósitos utilizada por el motor de base de datos para informar a la aplicación de un evento que implica las notificaciones de estado de cursor y desfragmentación en línea.</span><span class="sxs-lookup"><span data-stu-id="325cf-104">A multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="325cf-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="325cf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="325cf-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="325cf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="325cf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="325cf-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a><span data-ttu-id="325cf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="325cf-108">Parameters</span></span>

  - <span data-ttu-id="325cf-109">sesid</span><span class="sxs-lookup"><span data-stu-id="325cf-109">sesid</span></span>  
    <span data-ttu-id="325cf-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="325cf-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="325cf-111">Sesión para la que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-111">The session for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-112">dbid</span><span class="sxs-lookup"><span data-stu-id="325cf-112">dbid</span></span>  
    <span data-ttu-id="325cf-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="325cf-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="325cf-114">La base de datos para la que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-114">The database for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="325cf-115">tableid</span></span>  
    <span data-ttu-id="325cf-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="325cf-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="325cf-117">Cursor para el que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-117">The cursor for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-118">cbtyp</span><span class="sxs-lookup"><span data-stu-id="325cf-118">cbtyp</span></span>  
    <span data-ttu-id="325cf-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="325cf-119">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="325cf-120">Operación para la que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-120">The operation for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-121">arg1</span><span class="sxs-lookup"><span data-stu-id="325cf-121">arg1</span></span>  
    <span data-ttu-id="325cf-122">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="325cf-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="325cf-123">Primer argumento específico de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-123">First callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-124">arg2</span><span class="sxs-lookup"><span data-stu-id="325cf-124">arg2</span></span>  
    <span data-ttu-id="325cf-125">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="325cf-125">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="325cf-126">Segundo argumento específico de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-126">Second callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-127">context</span><span class="sxs-lookup"><span data-stu-id="325cf-127">context</span></span>  
    <span data-ttu-id="325cf-128">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="325cf-128">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="325cf-129">Contexto de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="325cf-129">Callback context.</span></span>

<!-- end list -->

  - <span data-ttu-id="325cf-130">unused</span><span class="sxs-lookup"><span data-stu-id="325cf-130">unused</span></span>  
    <span data-ttu-id="325cf-131">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="325cf-131">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="325cf-132">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="325cf-132">This parameter is not used.</span></span>

#### <a name="return-value"></a><span data-ttu-id="325cf-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="325cf-133">Return value</span></span>

<span data-ttu-id="325cf-134">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="325cf-134">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="325cf-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="325cf-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="325cf-136">Referencia</span><span class="sxs-lookup"><span data-stu-id="325cf-136">Reference</span></span>

[<span data-ttu-id="325cf-137">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="325cf-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
