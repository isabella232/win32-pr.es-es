---
description: El identificador de archivo único, también conocido como el número de referencia del archivo.
ms.assetid: 65189671-1b55-4933-9dee-a120b38caa98
title: System. FileFRN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aa536e0cdda3f42fd9e03315156716ef499c5f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659905"
---
# <a name="systemfilefrn"></a><span data-ttu-id="14f87-103">System. FileFRN</span><span class="sxs-lookup"><span data-stu-id="14f87-103">System.FileFRN</span></span>

<span data-ttu-id="14f87-104">El identificador de archivo único, también conocido como el número de referencia del archivo.</span><span class="sxs-lookup"><span data-stu-id="14f87-104">The unique file ID, also known as the File Reference Number.</span></span> <span data-ttu-id="14f87-105">Para un archivo determinado, se trata del mismo valor que el miembro **FileId** del ID. de archivo de la estructura de la [**\_ \_ \_ \_ información de dir**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) , que se obtiene mediante una llamada a [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span><span class="sxs-lookup"><span data-stu-id="14f87-105">For a given file, this is the same value as the **FileId** member of the [**FILE\_ID\_BOTH\_DIR\_INFO**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) structure, which is obtained by a call to [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="14f87-106">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14f87-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileFRN
   shellPKey = PKEY_FileFRN
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 21
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="14f87-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14f87-107">Remarks</span></span>

<span data-ttu-id="14f87-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="14f87-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14f87-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14f87-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14f87-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="14f87-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="14f87-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="14f87-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="14f87-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="14f87-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="14f87-113">Requerida</span><span class="sxs-lookup"><span data-stu-id="14f87-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="14f87-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="14f87-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="14f87-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="14f87-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="14f87-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="14f87-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="14f87-117">Numérico</span><span class="sxs-lookup"><span data-stu-id="14f87-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="14f87-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="14f87-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="14f87-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="14f87-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="14f87-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="14f87-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="14f87-121">editControl</span><span class="sxs-lookup"><span data-stu-id="14f87-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="14f87-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="14f87-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="14f87-123">Consulta</span><span class="sxs-lookup"><span data-stu-id="14f87-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
