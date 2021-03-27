---
description: La \_ \_ clase de nombre FileIo V0 es una versión anterior de la clase de tipo de evento para los eventos de e/s de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816259"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="8524f-104">\_Clase de \_ nombre V0 FileIo</span><span class="sxs-lookup"><span data-stu-id="8524f-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="8524f-105">La clase de **\_ \_ nombre FileIo V0** es una versión anterior de la clase de tipo de evento para los eventos de e/s de archivo.</span><span class="sxs-lookup"><span data-stu-id="8524f-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="8524f-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="8524f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8524f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8524f-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="8524f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8524f-108">Members</span></span>

<span data-ttu-id="8524f-109">La clase de **\_ \_ nombre FileIo V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8524f-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="8524f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8524f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8524f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8524f-111">Properties</span></span>

<span data-ttu-id="8524f-112">La clase de **\_ \_ nombre FileIo V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8524f-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8524f-113">FileName</span><span class="sxs-lookup"><span data-stu-id="8524f-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8524f-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8524f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8524f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8524f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8524f-116">Calificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="8524f-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="8524f-117">Ruta de acceso completa al archivo, sin incluir la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="8524f-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="8524f-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="8524f-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8524f-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8524f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8524f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8524f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8524f-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="8524f-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8524f-122">Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="8524f-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8524f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8524f-123">Remarks</span></span>

<span data-ttu-id="8524f-124">**Windows Server 2003:** Para recuperar la letra de unidad de la ruta de acceso del nombre de archivo, use el valor de la propiedad **FileObject** para asignar al evento [**\_ TypeGroup1 de desmontaje**](diskio-typegroup1.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8524f-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="8524f-125">En el **evento \_ desmontaje TypeGroup1** , use los valores de las propiedades **númerodedisco corresponde** y **byteoffset (** para asignar al evento [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8524f-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="8524f-126">La propiedad **DriveLetterString** contiene la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="8524f-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8524f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8524f-127">Requirements</span></span>



| <span data-ttu-id="8524f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8524f-128">Requirement</span></span> | <span data-ttu-id="8524f-129">Value</span><span class="sxs-lookup"><span data-stu-id="8524f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8524f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8524f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8524f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8524f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8524f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8524f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8524f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8524f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8524f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8524f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8524f-135">**FileIo \_ v0**</span><span class="sxs-lookup"><span data-stu-id="8524f-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




