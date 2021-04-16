---
description: 'Más información sobre: método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, cadena, JET_OBJECTINFO)'
title: Método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, cadena, JET_OBJECTINFO)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01311dcfbba226405a3c46c1be4c4553eac4eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696308"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a><span data-ttu-id="3bab4-103">Método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, cadena, JET_OBJECTINFO)</span><span class="sxs-lookup"><span data-stu-id="3bab4-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</span></span>

<span data-ttu-id="3bab4-104">Recupera información acerca de los objetos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="3bab4-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="3bab4-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3bab4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3bab4-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3bab4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3bab4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bab4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="3bab4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bab4-108">Parameters</span></span>

  - <span data-ttu-id="3bab4-109">sesid</span><span class="sxs-lookup"><span data-stu-id="3bab4-109">sesid</span></span>  
    <span data-ttu-id="3bab4-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3bab4-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3bab4-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3bab4-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bab4-112">dbid</span><span class="sxs-lookup"><span data-stu-id="3bab4-112">dbid</span></span>  
    <span data-ttu-id="3bab4-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3bab4-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="3bab4-114">Base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3bab4-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bab4-115">objtyp</span><span class="sxs-lookup"><span data-stu-id="3bab4-115">objtyp</span></span>  
    <span data-ttu-id="3bab4-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3bab4-116">Type: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="3bab4-117">Tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="3bab4-117">The type of the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bab4-118">objectName</span><span class="sxs-lookup"><span data-stu-id="3bab4-118">objectName</span></span>  
    <span data-ttu-id="3bab4-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3bab4-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3bab4-120">Nombre del objeto sobre el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="3bab4-120">The object name about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bab4-121">objectinfo</span><span class="sxs-lookup"><span data-stu-id="3bab4-121">objectinfo</span></span>  
    <span data-ttu-id="3bab4-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="3bab4-122">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="3bab4-123">Se rellena con información acerca de los objetos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3bab4-123">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bab4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bab4-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3bab4-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="3bab4-125">Reference</span></span>

[<span data-ttu-id="3bab4-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="3bab4-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3bab4-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="3bab4-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3bab4-128">Sobrecarga JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="3bab4-128">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="3bab4-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3bab4-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
