---
description: 'FileIo_Name clase : esta clase es la clase de tipo de evento para eventos de E/S de archivo. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: FileIo_Name clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9fabfbcfa318ad809b5cb2f66d72f19abf21112d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106593"
---
# <a name="fileio_name-class"></a><span data-ttu-id="a47e3-104">FileIo \_ Name (clase)</span><span class="sxs-lookup"><span data-stu-id="a47e3-104">FileIo\_Name class</span></span>

<span data-ttu-id="a47e3-105">Esta clase es la clase de tipo de evento para eventos de E/S de archivo.</span><span class="sxs-lookup"><span data-stu-id="a47e3-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="a47e3-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="a47e3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a47e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a47e3-107">Syntax</span></span>

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="a47e3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a47e3-108">Members</span></span>

<span data-ttu-id="a47e3-109">La **clase FileIo \_ Name** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a47e3-109">The **FileIo\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="a47e3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a47e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a47e3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a47e3-111">Properties</span></span>

<span data-ttu-id="a47e3-112">La **clase FileIo \_ Name** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a47e3-112">The **FileIo\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a47e3-113">FileName</span><span class="sxs-lookup"><span data-stu-id="a47e3-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47e3-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a47e3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a47e3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a47e3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a47e3-116">Calificadores: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="a47e3-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a47e3-117">Ruta de acceso completa al archivo, sin incluir la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="a47e3-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="a47e3-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="a47e3-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47e3-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="a47e3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a47e3-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a47e3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a47e3-121">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="a47e3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a47e3-122">Coincide con el valor de este puntero con el valor de puntero **FileObject** de un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de E/S.</span><span class="sxs-lookup"><span data-stu-id="a47e3-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a47e3-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a47e3-123">Remarks</span></span>

<span data-ttu-id="a47e3-124">**Windows Server 2003:** Para recuperar la letra de unidad de la ruta de acceso del nombre de archivo, use el valor de la propiedad **FileObject** para asignar al evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a47e3-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="a47e3-125">En el evento DiskIo TypeGroup1, use los valores de propiedad \_ **DiskNumber** y **ByteOffset** para asignar al evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondiente (**ByteOffset** se asigna a **StartOffset**).</span><span class="sxs-lookup"><span data-stu-id="a47e3-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="a47e3-126">La **propiedad DriveLetterString** contiene la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="a47e3-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a47e3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a47e3-127">Requirements</span></span>



| <span data-ttu-id="a47e3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a47e3-128">Requirement</span></span> | <span data-ttu-id="a47e3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a47e3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a47e3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a47e3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a47e3-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a47e3-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a47e3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a47e3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a47e3-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a47e3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a47e3-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a47e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a47e3-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="a47e3-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




