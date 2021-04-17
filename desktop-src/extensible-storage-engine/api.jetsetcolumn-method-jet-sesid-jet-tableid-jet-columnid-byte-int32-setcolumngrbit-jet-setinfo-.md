---
description: 'Más información sobre: método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, SetColumnGrbit, JET_SETINFO)'
title: Método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717110"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="3fcbd-103">Método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, SetColumnGrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="3fcbd-104">La función JetSetColumn modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="3fcbd-105">Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores en una columna con varios valores, quitar un valor de una secuencia de valores de una columna con varios valores o actualizar todo o parte de un valor Long (una columna de tipo [LongText](./jet-coltyp-enumeration.md) o [LongBinary](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="3fcbd-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="3fcbd-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3fcbd-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3fcbd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fcbd-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="3fcbd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fcbd-109">Parameters</span></span>

  - <span data-ttu-id="3fcbd-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3fcbd-110">sesid</span></span>  
    <span data-ttu-id="3fcbd-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3fcbd-112">La sesión que está realizando la actualización.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fcbd-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="3fcbd-113">tableid</span></span>  
    <span data-ttu-id="3fcbd-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3fcbd-115">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-115">The cursor to update.</span></span> <span data-ttu-id="3fcbd-116">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fcbd-117">columnid</span><span class="sxs-lookup"><span data-stu-id="3fcbd-117">columnid</span></span>  
    <span data-ttu-id="3fcbd-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3fcbd-119">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fcbd-120">datos</span><span class="sxs-lookup"><span data-stu-id="3fcbd-120">data</span></span>  
    <span data-ttu-id="3fcbd-121">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="3fcbd-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="3fcbd-122">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fcbd-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="3fcbd-123">dataSize</span></span>  
    <span data-ttu-id="3fcbd-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3fcbd-125">Tamaño de los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fcbd-126">grbit</span><span class="sxs-lookup"><span data-stu-id="3fcbd-126">grbit</span></span>  
    <span data-ttu-id="3fcbd-127">Tipo: [Microsoft. ISAM. esent. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-127">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3fcbd-128">Opciones de SetColumn.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-128">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="3fcbd-129">SetInfo</span><span class="sxs-lookup"><span data-stu-id="3fcbd-129">setinfo</span></span>  
    <span data-ttu-id="3fcbd-130">Tipo: [Microsoft.ISAM.esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-130">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="3fcbd-131">Se usa para especificar el desplazamiento de iTag o de valor largo.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-131">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3fcbd-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fcbd-132">Return value</span></span>

<span data-ttu-id="3fcbd-133">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3fcbd-133">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="3fcbd-134">Código de advertencia.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-134">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="3fcbd-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fcbd-135">Remarks</span></span>

<span data-ttu-id="3fcbd-136">Los métodos SetColumn proporcionan invalidaciones específicas del tipo de información que pueden ser más eficaces.</span><span class="sxs-lookup"><span data-stu-id="3fcbd-136">The SetColumn methods provide datatype-specific overrides which may be more efficient.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fcbd-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fcbd-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3fcbd-138">Referencia</span><span class="sxs-lookup"><span data-stu-id="3fcbd-138">Reference</span></span>

[<span data-ttu-id="3fcbd-139">Clase de API</span><span class="sxs-lookup"><span data-stu-id="3fcbd-139">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3fcbd-140">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="3fcbd-140">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3fcbd-141">Sobrecarga JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="3fcbd-141">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="3fcbd-142">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3fcbd-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
