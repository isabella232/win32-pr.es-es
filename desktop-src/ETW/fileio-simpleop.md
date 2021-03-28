---
description: Esta clase es la clase de tipo de evento para los eventos de operación de archivo simples. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: FileIo_SimpleOp (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985842"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="0eb81-104">\_Clase FileIo SimpleOp</span><span class="sxs-lookup"><span data-stu-id="0eb81-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="0eb81-105">Esta clase es la clase de tipo de evento para los eventos de operación de archivo simples.</span><span class="sxs-lookup"><span data-stu-id="0eb81-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="0eb81-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="0eb81-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb81-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0eb81-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="0eb81-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0eb81-108">Members</span></span>

<span data-ttu-id="0eb81-109">La clase **FileIo \_ SimpleOp** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0eb81-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="0eb81-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0eb81-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0eb81-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0eb81-111">Properties</span></span>

<span data-ttu-id="0eb81-112">La clase **FileIo \_ SimpleOp** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0eb81-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0eb81-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="0eb81-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb81-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0eb81-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0eb81-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-116">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="0eb81-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0eb81-117">Para determinar el nombre de archivo, haga coincidir el valor de esta propiedad con la propiedad **FileObject** de un evento de [**\_ nombre FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="0eb81-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="0eb81-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="0eb81-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb81-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0eb81-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0eb81-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-121">Calificadores: WmiDataId (3), puntero</span><span class="sxs-lookup"><span data-stu-id="0eb81-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0eb81-122">Identificador que se puede utilizar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre los eventos de creación y cierre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0eb81-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="0eb81-123">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="0eb81-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb81-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0eb81-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0eb81-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-126">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="0eb81-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0eb81-127">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="0eb81-127">IO request packet.</span></span> <span data-ttu-id="0eb81-128">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="0eb81-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="0eb81-129">**TTID**</span><span class="sxs-lookup"><span data-stu-id="0eb81-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb81-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0eb81-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0eb81-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb81-132">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="0eb81-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0eb81-133">Identificador de subproceso del subproceso que está realizando la operación.</span><span class="sxs-lookup"><span data-stu-id="0eb81-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0eb81-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0eb81-134">Remarks</span></span>

<span data-ttu-id="0eb81-135">El evento de limpieza se registra cuando se cierra el último identificador del archivo.</span><span class="sxs-lookup"><span data-stu-id="0eb81-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="0eb81-136">El evento Close especifica que se va a liberar un objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="0eb81-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="0eb81-137">El evento Flush especifica cuándo se vacían por completo los búferes de archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="0eb81-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb81-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0eb81-138">Requirements</span></span>



| <span data-ttu-id="0eb81-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eb81-139">Requirement</span></span> | <span data-ttu-id="0eb81-140">Value</span><span class="sxs-lookup"><span data-stu-id="0eb81-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0eb81-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0eb81-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb81-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0eb81-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0eb81-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0eb81-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb81-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0eb81-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0eb81-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="0eb81-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eb81-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="0eb81-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




