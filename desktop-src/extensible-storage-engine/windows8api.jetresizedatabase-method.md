---
description: 'Más información sobre: Windows8Api. JetResizeDatabase (método)'
title: Método Windows8Api. JetResizeDatabase (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetResizeDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetresizedatabase(v=EXCHG.10)
ms:contentKeyID: 55104462
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcca9a4006f8c8da1758a85d12d716b5ce1bba23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543643"
---
# <a name="windows8apijetresizedatabase-method"></a><span data-ttu-id="8d11a-103">Windows8Api. JetResizeDatabase, método</span><span class="sxs-lookup"><span data-stu-id="8d11a-103">Windows8Api.JetResizeDatabase method</span></span>

<span data-ttu-id="8d11a-104">Cambia el tamaño de una base de datos abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="8d11a-104">Resizes a currently open database.</span></span>

<span data-ttu-id="8d11a-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8d11a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8d11a-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8d11a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8d11a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d11a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResizeDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer, _
    grbit As ResizeDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As Integer
Dim grbit As ResizeDatabaseGrbitWindows8Api.JetResizeDatabase(sesid, dbid, _
    desiredPages, actualPages, grbit)
```

``` csharp
public static void JetResizeDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages,
    ResizeDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8d11a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d11a-108">Parameters</span></span>

  - <span data-ttu-id="8d11a-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8d11a-109">sesid</span></span>  
    <span data-ttu-id="8d11a-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8d11a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8d11a-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="8d11a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8d11a-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8d11a-112">dbid</span></span>  
    <span data-ttu-id="8d11a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8d11a-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8d11a-114">Base de datos que se va a aumentar.</span><span class="sxs-lookup"><span data-stu-id="8d11a-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="8d11a-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="8d11a-115">desiredPages</span></span>  
    <span data-ttu-id="8d11a-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8d11a-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8d11a-117">Tamaño deseado de la base de datos, en páginas.</span><span class="sxs-lookup"><span data-stu-id="8d11a-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="8d11a-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="8d11a-118">actualPages</span></span>  
    <span data-ttu-id="8d11a-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8d11a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8d11a-120">Tamaño de la base de datos, en páginas, después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8d11a-120">The size of the database, in pages, after the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="8d11a-121">grbit</span><span class="sxs-lookup"><span data-stu-id="8d11a-121">grbit</span></span>  
    <span data-ttu-id="8d11a-122">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8d11a-122">Type: [Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8d11a-123">Opciones de cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="8d11a-123">Resize options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d11a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d11a-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8d11a-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="8d11a-125">Reference</span></span>

[<span data-ttu-id="8d11a-126">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="8d11a-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="8d11a-127">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="8d11a-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="8d11a-128">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="8d11a-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
