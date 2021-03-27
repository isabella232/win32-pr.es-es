---
description: Esta clase es la clase de tipo de evento para los eventos de e/s de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082943"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="83b6c-104">\_Clase de \_ nombre FileIo v1</span><span class="sxs-lookup"><span data-stu-id="83b6c-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="83b6c-105">Esta clase es la clase de tipo de evento para los eventos de e/s de archivo.</span><span class="sxs-lookup"><span data-stu-id="83b6c-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="83b6c-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="83b6c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b6c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83b6c-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="83b6c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="83b6c-108">Members</span></span>

<span data-ttu-id="83b6c-109">La clase de **\_ \_ nombre FileIo v1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="83b6c-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="83b6c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83b6c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83b6c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83b6c-111">Properties</span></span>

<span data-ttu-id="83b6c-112">La clase de **\_ \_ nombre FileIo v1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="83b6c-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83b6c-113">FileName</span><span class="sxs-lookup"><span data-stu-id="83b6c-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b6c-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83b6c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83b6c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83b6c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83b6c-116">Calificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="83b6c-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="83b6c-117">Ruta de acceso completa al archivo, sin incluir la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="83b6c-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="83b6c-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="83b6c-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b6c-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83b6c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83b6c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83b6c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83b6c-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="83b6c-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="83b6c-122">Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="83b6c-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83b6c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83b6c-123">Remarks</span></span>

<span data-ttu-id="83b6c-124">**Windows Server 2003:** Para recuperar la letra de unidad de la ruta de acceso del nombre de archivo, use el valor de la propiedad **FileObject** para asignar al evento [ \_ TypeGroup1 de desmontaje](diskio-typegroup1.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="83b6c-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="83b6c-125">En el \_ evento desmontaje TypeGroup1, use los valores de las propiedades **Númerodedisco corresponde** y **byteoffset (** para asignar al evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondiente (**byteoffset (** se asigna a **StartOffset**).</span><span class="sxs-lookup"><span data-stu-id="83b6c-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="83b6c-126">La propiedad **DriveLetterString** contiene la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="83b6c-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b6c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83b6c-127">Requirements</span></span>



| <span data-ttu-id="83b6c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b6c-128">Requirement</span></span> | <span data-ttu-id="83b6c-129">Value</span><span class="sxs-lookup"><span data-stu-id="83b6c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83b6c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83b6c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83b6c-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="83b6c-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="83b6c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83b6c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83b6c-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83b6c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83b6c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="83b6c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b6c-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="83b6c-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




