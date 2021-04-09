---
description: Almacena el estado de las respuestas de un usuario a las reuniones en el calendario.
ms.assetid: 5cbc0306-20c7-4f12-bb8b-3889b93dfd69
title: System. Calendar. ResponseStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af8f69d177dba751ead02a0ee71f5ea4a42ae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155941"
---
# <a name="systemcalendarresponsestatus"></a><span data-ttu-id="3755f-103">System. Calendar. ResponseStatus</span><span class="sxs-lookup"><span data-stu-id="3755f-103">System.Calendar.ResponseStatus</span></span>

<span data-ttu-id="3755f-104">Almacena el estado de las respuestas de un usuario a las reuniones en el calendario.</span><span class="sxs-lookup"><span data-stu-id="3755f-104">Stores the status of a user's responses to meetings in the calendar.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="3755f-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="3755f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Calendar.ResponseStatus
   shellPKey = PKEY_Calendar_ResponseStatus
   formatID = 188C1F91-3C40-4132-9EC5-D8B03B72A8A2
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = None
            defineToken = CALENDAR_RESPONSESTATUS_NONE
         enum
            name = Organized
            value = 1
            text = Organized
            defineToken = CALENDAR_RESPONSESTATUS_ORGANIZED
         enum
            name = Tentative
            value = 2
            text = Tentative
            defineToken = CALENDAR_RESPONSESTATUS_TENTATIVE
         enum
            name = Accepted
            value = 3
            text = Accepted
            defineToken = CALENDAR_RESPONSESTATUS_ACCEPTED
         enum
            name = Declined
            value = 4
            text = Declined
            defineToken = CALENDAR_RESPONSESTATUS_DECLINED
         enum
            name = NotResponded
            value = 5
            text = Not Responded
            defineToken = CALENDAR_RESPONSESTATUS_NOTRESPONDED
```

## <a name="windows-vista"></a><span data-ttu-id="3755f-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3755f-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Calendar.ResponseStatus
   shellPKey = PKEY_Calendar_ResponseStatus
   formatID = 188C1F91-3C40-4132-9EC5-D8B03B72A8A2
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = None
            defineName = CALENDAR_RESPONSESTATUS_NONE
         enum
            value = 1
            text = Organized
            defineName = CALENDAR_RESPONSESTATUS_ORGANIZED
         enum
            value = 2
            text = Tentative
            defineName = CALENDAR_RESPONSESTATUS_TENTATIVE
         enum
            value = 3
            text = Accepted
            defineName = CALENDAR_RESPONSESTATUS_ACCEPTED
         enum
            value = 4
            text = Declined
            defineName = CALENDAR_RESPONSESTATUS_DECLINED
         enum
            value = 5
            text = Not Responded
            defineName = CALENDAR_RESPONSESTATUS_NOTRESPONDED
```

## <a name="remarks"></a><span data-ttu-id="3755f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3755f-107">Remarks</span></span>

<span data-ttu-id="3755f-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="3755f-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3755f-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3755f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3755f-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3755f-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3755f-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3755f-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3755f-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3755f-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3755f-113">Requerida</span><span class="sxs-lookup"><span data-stu-id="3755f-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3755f-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3755f-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3755f-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3755f-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3755f-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3755f-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3755f-117">Numérico</span><span class="sxs-lookup"><span data-stu-id="3755f-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3755f-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3755f-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3755f-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3755f-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3755f-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="3755f-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3755f-121">editControl</span><span class="sxs-lookup"><span data-stu-id="3755f-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3755f-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="3755f-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3755f-123">Consulta</span><span class="sxs-lookup"><span data-stu-id="3755f-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
