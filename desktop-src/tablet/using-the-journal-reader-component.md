---
description: El componente lector de notas de Microsoft Windows Journal proporciona acceso de lectura mediante programación a los archivos en formato de diario.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Usar el componente de lector de Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001111"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="ca937-103">Usar el componente de lector de Journal</span><span class="sxs-lookup"><span data-stu-id="ca937-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="ca937-104">El componente lector de notas de Microsoft Windows Journal proporciona acceso de lectura mediante programación a los archivos en formato de diario.</span><span class="sxs-lookup"><span data-stu-id="ca937-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="ca937-105">Información general del componente</span><span class="sxs-lookup"><span data-stu-id="ca937-105">Component Overview</span></span>

<span data-ttu-id="ca937-106">Los archivos de diario tienen la extensión de archivo. JNT.</span><span class="sxs-lookup"><span data-stu-id="ca937-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="ca937-107">Este componente simple toma una secuencia que contiene un archivo. JNT y devuelve una secuencia que contiene el contenido del archivo en formato XML.</span><span class="sxs-lookup"><span data-stu-id="ca937-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="ca937-108">El XML devuelto por el componente se ajusta al esquema lector de notas de Journal.</span><span class="sxs-lookup"><span data-stu-id="ca937-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="ca937-109">Este esquema se documenta en [referencia de esquema del lector de diarios](journal-reader-schema-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ca937-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="ca937-110">El componente no proporciona la capacidad de escribir archivos. JNT.</span><span class="sxs-lookup"><span data-stu-id="ca937-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="ca937-111">El componente está disponible en las versiones administradas y no administradas.</span><span class="sxs-lookup"><span data-stu-id="ca937-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="ca937-112">El componente no administrado está disponible en la journal.dll biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="ca937-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="ca937-113">La versión administrada se encuentra en el Microsoft.Ink.Journal.dll ensamblado (para la redistribución a Windows XP Tablet PC Edition o Windows Vista) o Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="ca937-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ca937-114">A partir de Windows 10, versión 1607, journal.dll no se incluye en el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="ca937-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="ca937-115">Esa biblioteca debe considerarse en desuso u obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ca937-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="ca937-116">Cambios de ensamblado de nota</span><span class="sxs-lookup"><span data-stu-id="ca937-116">Assembly Changes of Note</span></span>

<span data-ttu-id="ca937-117">Es importante tener en cuenta algunos cambios en el ensamblado que contiene el componente lector de notas de Journal que se produjo entre la versión publicada junto con la versión 1,7 del kit para desarrolladores de Tablet PC y la versión que se incluye en el sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca937-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="ca937-118">La versión 1,7 del componente lector, que se puede redistribuir a Windows XP o Windows Vista, se encuentra en un ensamblado denominado Microsoft.Ink.Journal.dll.</span><span class="sxs-lookup"><span data-stu-id="ca937-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="ca937-119">El componente lector se incluye en Windows Vista, pero se ha integrado en el ensamblado principal de Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="ca937-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="ca937-120">Esto significa que las aplicaciones que usan el ensamblado 1,7 deben redistribuir ese ensamblado con su configuración.</span><span class="sxs-lookup"><span data-stu-id="ca937-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="ca937-121">Usar el componente</span><span class="sxs-lookup"><span data-stu-id="ca937-121">Using the Component</span></span>

<span data-ttu-id="ca937-122">El componente lector de notas de Journal es útil para extraer los datos de tinta y otra información sobre el archivo de un archivo de diario.</span><span class="sxs-lookup"><span data-stu-id="ca937-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="ca937-123">COM</span><span class="sxs-lookup"><span data-stu-id="ca937-123">COM</span></span>

<span data-ttu-id="ca937-124">El componente COM lector de notas de Journal está en el archivo Journal.dll, que se instala y registra al descargar y ejecutar el archivo de instalación del lector de notas de Journal.</span><span class="sxs-lookup"><span data-stu-id="ca937-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="ca937-125">El componente COM no admite la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ca937-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="ca937-126">Administrado</span><span class="sxs-lookup"><span data-stu-id="ca937-126">Managed</span></span>

<span data-ttu-id="ca937-127">El componente administrado lector de notas de Journal está en el ensamblado de Microsoft.Ink.JournalReader.dll.</span><span class="sxs-lookup"><span data-stu-id="ca937-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="ca937-128">Este ensamblado se instala y registra en la caché global de ensamblados al ejecutar el archivo de instalación del lector de notas de Journal.</span><span class="sxs-lookup"><span data-stu-id="ca937-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="ca937-129">Agregue una referencia al ensamblado para usarlo en el proyecto administrado.</span><span class="sxs-lookup"><span data-stu-id="ca937-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca937-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca937-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca937-131">**Interfaz IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="ca937-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="ca937-132">Referencia del esquema del lector de Journal</span><span class="sxs-lookup"><span data-stu-id="ca937-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
