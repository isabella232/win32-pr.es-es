---
description: 'Más información acerca de: JET_CALLBACK función de devolución de llamada'
title: JET_CALLBACK función de devolución de llamada
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677500"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="8a725-103">JET_CALLBACK función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="8a725-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="8a725-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8a725-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="8a725-105">JET_CALLBACK función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="8a725-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="8a725-106">La función **JET_CALLBACK** es una función de devolución de llamada de varios propósitos utilizada por el motor de base de datos para informar a la aplicación de un evento que implique las notificaciones de estado de cursor y desfragmentación en línea.</span><span class="sxs-lookup"><span data-stu-id="8a725-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="8a725-107">Vea [JET_CBTYP](./jet-cbtyp.md) para ver la configuración específica para los parámetros de esta función, ya que estas opciones variarán en función de la opción **JET_CBTYP** seleccionada para su uso en el parámetro *CBTYP* .</span><span class="sxs-lookup"><span data-stu-id="8a725-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="8a725-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a725-108">Parameters</span></span>

<span data-ttu-id="8a725-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8a725-109">*sesid*</span></span>

<span data-ttu-id="8a725-110">Sesión para la que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="8a725-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="8a725-111">*dbid*</span></span>

<span data-ttu-id="8a725-112">La base de datos para la que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="8a725-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="8a725-113">*tableid*</span></span>

<span data-ttu-id="8a725-114">Cursor para el que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="8a725-115">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="8a725-115">*cbtyp*</span></span>

<span data-ttu-id="8a725-116">Punto de la operación en el que se realiza la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="8a725-117">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener una lista de valores y el significado de los parámetros siguientes en cada caso.</span><span class="sxs-lookup"><span data-stu-id="8a725-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="8a725-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="8a725-118">*pvArg1*</span></span>

<span data-ttu-id="8a725-119">Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="8a725-120">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8a725-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="8a725-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="8a725-121">*pvArg2*</span></span>

<span data-ttu-id="8a725-122">Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="8a725-123">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8a725-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="8a725-124">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="8a725-124">*pvContext*</span></span>

<span data-ttu-id="8a725-125">Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="8a725-126">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8a725-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="8a725-127">*ulUnused*</span><span class="sxs-lookup"><span data-stu-id="8a725-127">*ulUnused*</span></span>

<span data-ttu-id="8a725-128">Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="8a725-129">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8a725-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8a725-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a725-130">Return Value</span></span>

<span data-ttu-id="8a725-131">La función devuelve uno de los [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8a725-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="8a725-132">Para obtener información sobre cómo devolver estos códigos como valores HRESULT, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="8a725-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="8a725-133">Si se ejecuta correctamente, la operación que emitió la devolución de llamada puede continuar con normalidad.</span><span class="sxs-lookup"><span data-stu-id="8a725-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="8a725-134">En algunos casos, la devolución de llamada puede devolver una advertencia que influye en esa operación.</span><span class="sxs-lookup"><span data-stu-id="8a725-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="8a725-135">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de estas advertencias en la operación.</span><span class="sxs-lookup"><span data-stu-id="8a725-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="8a725-136">En caso de error, la operación que ha emitido la devolución de llamada puede continuar normalmente o puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="8a725-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="8a725-137">Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso del código de error en la operación.</span><span class="sxs-lookup"><span data-stu-id="8a725-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8a725-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a725-138">Remarks</span></span>

<span data-ttu-id="8a725-139">Si la devolución de llamada pasa un cursor a la aplicación, es importante saber que este cursor está limitado intencionadamente a un conjunto más pequeño de funciones para evitar la recursividad y otros ugliness.</span><span class="sxs-lookup"><span data-stu-id="8a725-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="8a725-140">Se permiten las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="8a725-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="8a725-141">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="8a725-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="8a725-142">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="8a725-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="8a725-143">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="8a725-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="8a725-144">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="8a725-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="8a725-145">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="8a725-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="8a725-146">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="8a725-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="8a725-147">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="8a725-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="8a725-148">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="8a725-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="8a725-149">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="8a725-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="8a725-150">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="8a725-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="8a725-151">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="8a725-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="8a725-152">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="8a725-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="8a725-153">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="8a725-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="8a725-154">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="8a725-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="8a725-155">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="8a725-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="8a725-156">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="8a725-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="8a725-157">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="8a725-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="8a725-158">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="8a725-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="8a725-159">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="8a725-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="8a725-160">Al diseñar la devolución de llamada, tenga en cuenta que incluso con estas restricciones, todavía es posible que se produzca un error en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8a725-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8a725-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a725-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a725-162"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8a725-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8a725-163">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8a725-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a725-164"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8a725-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8a725-165">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8a725-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a725-166"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8a725-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8a725-167">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8a725-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8a725-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a725-168">See Also</span></span>

[<span data-ttu-id="8a725-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="8a725-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="8a725-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="8a725-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="8a725-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8a725-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8a725-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8a725-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8a725-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="8a725-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
