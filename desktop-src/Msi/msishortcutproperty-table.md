---
description: La tabla MsiShortcutProperty habilita el instalador de Windows para establecer las propiedades de los accesos directos que también son objetos de Shell de Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabla MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546422"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="f488a-103">Tabla MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="f488a-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="f488a-104">La tabla MsiShortcutProperty habilita el instalador de Windows para establecer las propiedades de los accesos directos que también son objetos de [Shell de Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f488a-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="f488a-105">A partir de Windows Vista y Windows Server 2008, el shell de Windows proporciona una interfaz IPropertyStore para objetos de shell como métodos abreviados.</span><span class="sxs-lookup"><span data-stu-id="f488a-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="f488a-106">Un paquete Windows Installer 5,0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede establecer estas propiedades cuando se instala el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="f488a-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="f488a-107">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="f488a-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="f488a-108">Esta tabla está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="f488a-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="f488a-109">La tabla MsiShortcutProperty tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f488a-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="f488a-110">Columna</span><span class="sxs-lookup"><span data-stu-id="f488a-110">Column</span></span>              | <span data-ttu-id="f488a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f488a-111">Type</span></span>                         | <span data-ttu-id="f488a-112">Clave</span><span class="sxs-lookup"><span data-stu-id="f488a-112">Key</span></span> | <span data-ttu-id="f488a-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="f488a-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="f488a-114">MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="f488a-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="f488a-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="f488a-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f488a-116">Y</span><span class="sxs-lookup"><span data-stu-id="f488a-116">Y</span></span>   | <span data-ttu-id="f488a-117">N</span><span class="sxs-lookup"><span data-stu-id="f488a-117">N</span></span>        |
| <span data-ttu-id="f488a-118">Acceso directo\_</span><span class="sxs-lookup"><span data-stu-id="f488a-118">Shortcut\_</span></span>          | [<span data-ttu-id="f488a-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="f488a-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="f488a-120">N</span><span class="sxs-lookup"><span data-stu-id="f488a-120">N</span></span>   | <span data-ttu-id="f488a-121">N</span><span class="sxs-lookup"><span data-stu-id="f488a-121">N</span></span>        |
| <span data-ttu-id="f488a-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="f488a-122">PropertyKey</span></span>         | [<span data-ttu-id="f488a-123">Formatea</span><span class="sxs-lookup"><span data-stu-id="f488a-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f488a-124">N</span><span class="sxs-lookup"><span data-stu-id="f488a-124">N</span></span>   | <span data-ttu-id="f488a-125">N</span><span class="sxs-lookup"><span data-stu-id="f488a-125">N</span></span>        |
| <span data-ttu-id="f488a-126">PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="f488a-126">PropVariantValue</span></span>    | [<span data-ttu-id="f488a-127">Formatea</span><span class="sxs-lookup"><span data-stu-id="f488a-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f488a-128">N</span><span class="sxs-lookup"><span data-stu-id="f488a-128">N</span></span>   | <span data-ttu-id="f488a-129">N</span><span class="sxs-lookup"><span data-stu-id="f488a-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f488a-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="f488a-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f488a-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="f488a-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="f488a-132">Identificador único para esta fila de la tabla MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="f488a-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="f488a-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Contextual\_</span><span class="sxs-lookup"><span data-stu-id="f488a-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="f488a-134">Clave en la tabla de [accesos directos](shortcut-table.md) que identifica el acceso directo que tiene establecida una propiedad.</span><span class="sxs-lookup"><span data-stu-id="f488a-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="f488a-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="f488a-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="f488a-136">Valor de cadena que proporciona información para la estructura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) .</span><span class="sxs-lookup"><span data-stu-id="f488a-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="f488a-137">La información de este campo debe hacer referencia al nombre canónico de una propiedad registrada con el sistema de propiedades de Windows.</span><span class="sxs-lookup"><span data-stu-id="f488a-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="f488a-138">Para obtener más información sobre el sistema de propiedades de Windows, vea la [información general](/previous-versions//bb776909(v=vs.85))sobre el sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f488a-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f488a-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="f488a-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="f488a-140">Valor de cadena que proporciona información para la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="f488a-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="f488a-141">Se pueden establecer varias propiedades en un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="f488a-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="f488a-142">Si se establece la misma propiedad varias veces en el mismo método abreviado, el valor se establece en un orden no especificado.</span><span class="sxs-lookup"><span data-stu-id="f488a-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="f488a-143">Windows Installer puede establecer las propiedades de acceso directo solo cuando se instala o se vuelve a instalar el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="f488a-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="f488a-144">Una revisión que no Reinstala un acceso directo que ya se ha instalado no actualiza las propiedades del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="f488a-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="f488a-145">Una revisión puede actualizar las propiedades incluyendo una tabla de [acceso directo](shortcut-table.md) en el paquete de revisión y reinstalando el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="f488a-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="f488a-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f488a-146">Remarks</span></span>

<span data-ttu-id="f488a-147">[Windows Installer mensaje de Error](windows-installer-error-messages.md) 1946 se devuelve como una advertencia y la instalación continúa, si Windows Installer no puede establecer una propiedad de acceso directo especificada en la tabla MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="f488a-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="f488a-148">Validación</span><span class="sxs-lookup"><span data-stu-id="f488a-148">Validation</span></span>

<dl>

[<span data-ttu-id="f488a-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="f488a-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
