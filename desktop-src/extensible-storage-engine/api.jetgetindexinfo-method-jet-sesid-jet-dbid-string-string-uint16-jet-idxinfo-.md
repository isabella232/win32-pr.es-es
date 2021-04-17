---
description: 'Más información sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, UInt16, JET_IdxInfo)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 762437dba9e502de5c0650e4ae6df53d4629d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652391"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a><span data-ttu-id="fc443-103">Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="fc443-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="fc443-104">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="fc443-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="fc443-105">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="fc443-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="fc443-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc443-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fc443-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fc443-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc443-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc443-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="fc443-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc443-109">Parameters</span></span>

  - <span data-ttu-id="fc443-110">sesid</span><span class="sxs-lookup"><span data-stu-id="fc443-110">sesid</span></span>  
    <span data-ttu-id="fc443-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc443-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fc443-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="fc443-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc443-113">dbid</span><span class="sxs-lookup"><span data-stu-id="fc443-113">dbid</span></span>  
    <span data-ttu-id="fc443-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc443-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="fc443-115">Base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="fc443-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc443-116">tablename</span><span class="sxs-lookup"><span data-stu-id="fc443-116">tablename</span></span>  
    <span data-ttu-id="fc443-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="fc443-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="fc443-118">Nombre de la tabla sobre la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="fc443-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc443-119">IndexName</span><span class="sxs-lookup"><span data-stu-id="fc443-119">indexname</span></span>  
    <span data-ttu-id="fc443-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="fc443-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="fc443-121">Nombre del índice del que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="fc443-121">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc443-122">resultado</span><span class="sxs-lookup"><span data-stu-id="fc443-122">result</span></span>  
    <span data-ttu-id="fc443-123">Tipo: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="fc443-123">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="fc443-124">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="fc443-124">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc443-125">infoLevel</span><span class="sxs-lookup"><span data-stu-id="fc443-125">infoLevel</span></span>  
    <span data-ttu-id="fc443-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fc443-126">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="fc443-127">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="fc443-127">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc443-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc443-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc443-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="fc443-129">Reference</span></span>

[<span data-ttu-id="fc443-130">Clase de API</span><span class="sxs-lookup"><span data-stu-id="fc443-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fc443-131">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="fc443-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fc443-132">Sobrecarga JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="fc443-132">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="fc443-133">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fc443-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
