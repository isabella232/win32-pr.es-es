---
description: 'El prefijo de un elemento, que se usa para los mensajes de correo electrónico en los que el asunto comienza con el prefijo &\# 0034; Re: &\# 0034;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001344"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="36c51-103">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="36c51-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="36c51-104">El prefijo de un elemento, que se usa para los mensajes de correo electrónico en los que el asunto comienza con el prefijo "re:".</span><span class="sxs-lookup"><span data-stu-id="36c51-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="36c51-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36c51-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="36c51-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36c51-106">Remarks</span></span>

<span data-ttu-id="36c51-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="36c51-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="36c51-108">Si el elemento es un archivo, el valor de esta propiedad es VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="36c51-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="36c51-109">Si el elemento es un mensaje, el valor de esta propiedad son los prefijos de reenvío o respuesta (incluidos los dos puntos delimitadores, pero no hay espacios en blanco) o VT \_ vacío si no hay prefijo.</span><span class="sxs-lookup"><span data-stu-id="36c51-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="36c51-110">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="36c51-110">Example values:</span></span>



| <span data-ttu-id="36c51-111">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="36c51-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="36c51-112">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="36c51-112">System.ItemName</span></span>  | <span data-ttu-id="36c51-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="36c51-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="36c51-114">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="36c51-114">VT\_EMPTY</span></span>             | <span data-ttu-id="36c51-115">"Día excelente"</span><span class="sxs-lookup"><span data-stu-id="36c51-115">"Great day"</span></span>      | <span data-ttu-id="36c51-116">"Día excelente"</span><span class="sxs-lookup"><span data-stu-id="36c51-116">"Great day"</span></span>            |
| <span data-ttu-id="36c51-117">"Re:"</span><span class="sxs-lookup"><span data-stu-id="36c51-117">"Re:"</span></span>                 | <span data-ttu-id="36c51-118">"Día excelente"</span><span class="sxs-lookup"><span data-stu-id="36c51-118">"Great day"</span></span>      | <span data-ttu-id="36c51-119">"Re: excelente día"</span><span class="sxs-lookup"><span data-stu-id="36c51-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="36c51-120">"FWD:"</span><span class="sxs-lookup"><span data-stu-id="36c51-120">"Fwd: "</span></span>               | <span data-ttu-id="36c51-121">"Presupuesto mensual"</span><span class="sxs-lookup"><span data-stu-id="36c51-121">"Monthly budget"</span></span> | <span data-ttu-id="36c51-122">"FWD: Monthly Budget"</span><span class="sxs-lookup"><span data-stu-id="36c51-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="36c51-123">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="36c51-123">VT\_EMPTY</span></span>             | <span data-ttu-id="36c51-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="36c51-124">accounts.xls</span></span>     | <span data-ttu-id="36c51-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="36c51-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="36c51-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36c51-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36c51-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="36c51-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="36c51-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="36c51-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="36c51-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="36c51-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="36c51-130">Requerida</span><span class="sxs-lookup"><span data-stu-id="36c51-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="36c51-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="36c51-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="36c51-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="36c51-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="36c51-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="36c51-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="36c51-134">Numérico</span><span class="sxs-lookup"><span data-stu-id="36c51-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="36c51-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="36c51-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="36c51-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="36c51-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="36c51-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="36c51-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="36c51-138">editControl</span><span class="sxs-lookup"><span data-stu-id="36c51-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="36c51-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="36c51-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="36c51-140">Consulta</span><span class="sxs-lookup"><span data-stu-id="36c51-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
