---
description: Fecha de adquisición del archivo o medio.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278893"
---
# <a name="systemdateacquired"></a><span data-ttu-id="4aad0-103">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="4aad0-103">System.DateAcquired</span></span>

<span data-ttu-id="4aad0-104">Fecha de adquisición del archivo o medio.</span><span class="sxs-lookup"><span data-stu-id="4aad0-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="4aad0-105">Esta propiedad está relacionada con un usuario o grupo de usuarios determinado.</span><span class="sxs-lookup"><span data-stu-id="4aad0-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="4aad0-106">Por ejemplo, estos datos se usan como el eje principal de ordenación de la carpeta virtual **New Music**, que permite a los usuarios examinar las adiciones más recientes a su colección.</span><span class="sxs-lookup"><span data-stu-id="4aad0-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="4aad0-107">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4aad0-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="4aad0-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aad0-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="4aad0-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4aad0-109">Remarks</span></span>

<span data-ttu-id="4aad0-110">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="4aad0-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="4aad0-111">[DateAcquired]() se almacena como un valor en la secuencia principal del archivo, pero es posible que no siempre esté presente.</span><span class="sxs-lookup"><span data-stu-id="4aad0-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="4aad0-112">En esos casos, la fecha de adquisición se puede aproximar en función de otras fechas conocidas para el contenido.</span><span class="sxs-lookup"><span data-stu-id="4aad0-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="4aad0-113">El controlador de metadatos debe utilizar un conjunto de reglas para determinar la fecha que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="4aad0-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="4aad0-114">En el ejemplo siguiente se muestra esto para los archivos de música.</span><span class="sxs-lookup"><span data-stu-id="4aad0-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="4aad0-115">En el caso de la música comprada, se debe usar la hora de creación del archivo si no hay ninguna fecha adquirida.</span><span class="sxs-lookup"><span data-stu-id="4aad0-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="4aad0-116">Sin embargo, el proveedor de descargas debe establecer la propiedad [DateAcquired]() en el archivo.</span><span class="sxs-lookup"><span data-stu-id="4aad0-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="4aad0-117">En el caso de los archivos de música que el usuario o el grupo "copió" (copiando música o vídeo desde un CD o DVD a un disco duro), la fecha de adquisición debe ser la fecha en que tuvo lugar la acción.</span><span class="sxs-lookup"><span data-stu-id="4aad0-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="4aad0-118">Por ejemplo, el atributo [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4aad0-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="4aad0-119">En el caso de la música copiada desde otra ubicación, la hora de creación del archivo debe usarse como la fecha de adquisición.</span><span class="sxs-lookup"><span data-stu-id="4aad0-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="4aad0-120">Algunos ejemplos de [System. DateAcquired]() son la fecha y la hora en que se adquieren imágenes de una cámara o cuando la música se adquiere en línea.</span><span class="sxs-lookup"><span data-stu-id="4aad0-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="4aad0-121">No es lo mismo que [System. DateImported](./props-system-dateimported.md).</span><span class="sxs-lookup"><span data-stu-id="4aad0-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aad0-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4aad0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aad0-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4aad0-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4aad0-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4aad0-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4aad0-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4aad0-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4aad0-126">Requerida</span><span class="sxs-lookup"><span data-stu-id="4aad0-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4aad0-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4aad0-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4aad0-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4aad0-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4aad0-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4aad0-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4aad0-130">Numérico</span><span class="sxs-lookup"><span data-stu-id="4aad0-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4aad0-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4aad0-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4aad0-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4aad0-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4aad0-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="4aad0-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4aad0-134">editControl</span><span class="sxs-lookup"><span data-stu-id="4aad0-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4aad0-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="4aad0-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4aad0-136">Consulta</span><span class="sxs-lookup"><span data-stu-id="4aad0-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
