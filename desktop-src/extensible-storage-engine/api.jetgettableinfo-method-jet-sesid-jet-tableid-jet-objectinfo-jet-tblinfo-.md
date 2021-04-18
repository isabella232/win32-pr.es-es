---
description: 'Más información sobre: método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)'
title: Método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100739
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbc95c771e2610ec23bdf503cdefa0399ee219ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715431"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_objectinfo-jet_tblinfo"></a><span data-ttu-id="cc3f8-103">Método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</span></span>

<span data-ttu-id="cc3f8-104">Recupera varios fragmentos de información sobre una tabla de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="cc3f8-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cc3f8-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3f8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc3f8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_OBJECTINFO, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_OBJECTINFO
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_OBJECTINFO result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="cc3f8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc3f8-108">Parameters</span></span>

  - <span data-ttu-id="cc3f8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="cc3f8-109">sesid</span></span>  
    <span data-ttu-id="cc3f8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cc3f8-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc3f8-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="cc3f8-112">tableid</span></span>  
    <span data-ttu-id="cc3f8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cc3f8-114">Tabla de la que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc3f8-115">resultado</span><span class="sxs-lookup"><span data-stu-id="cc3f8-115">result</span></span>  
    <span data-ttu-id="cc3f8-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-116">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="cc3f8-117">Información recuperada.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc3f8-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="cc3f8-118">infoLevel</span></span>  
    <span data-ttu-id="cc3f8-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cc3f8-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="cc3f8-120">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="cc3f8-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc3f8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc3f8-121">Remarks</span></span>

<span data-ttu-id="cc3f8-122">Esta sobrecarga se usa con el [valor predeterminado](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="cc3f8-122">This overload is used with [Default](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc3f8-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc3f8-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cc3f8-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="cc3f8-124">Reference</span></span>

[<span data-ttu-id="cc3f8-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="cc3f8-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cc3f8-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="cc3f8-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cc3f8-127">Sobrecarga JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="cc3f8-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="cc3f8-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cc3f8-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
