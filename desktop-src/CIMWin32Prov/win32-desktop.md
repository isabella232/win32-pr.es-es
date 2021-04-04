---
description: La \_ clase DesktopWMI de Win32 representa las características comunes del escritorio de un usuario. El usuario puede modificar las propiedades de esta clase para personalizar el escritorio.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907525"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="c7f2d-104">\_Clase de escritorio Win32</span><span class="sxs-lookup"><span data-stu-id="c7f2d-104">Win32\_Desktop class</span></span>

<span data-ttu-id="c7f2d-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ escritorio Win32** representa las características comunes del escritorio de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="c7f2d-106">El usuario puede modificar las propiedades de esta clase para personalizar el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="c7f2d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c7f2d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f2d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7f2d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="c7f2d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7f2d-110">Members</span></span>

<span data-ttu-id="c7f2d-111">La clase de **\_ escritorio Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c7f2d-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="c7f2d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7f2d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7f2d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7f2d-113">Properties</span></span>

<span data-ttu-id="c7f2d-114">La clase de **\_ escritorio Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7f2d-115">**BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ \\ \\ WindowMetrics \| BorderWidth ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-119">Ancho de los bordes alrededor de todas las ventanas con bordes ajustables.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="c7f2d-120">Ejemplo: 3</span><span class="sxs-lookup"><span data-stu-id="c7f2d-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-124">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c7f2d-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-125">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-125">Short textual description of the current object.</span></span>

<span data-ttu-id="c7f2d-126">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c7f2d-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-127">**CoolSwitch**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry de \| escritorio del panel de control de \\ \\ \| CoolSwitch")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-131">La conmutación por tarea rápida está activada.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-131">Fast task switching is turned on.</span></span> <span data-ttu-id="c7f2d-132">El cambio rápido de tareas permite al usuario alternar entre ventanas mediante la combinación de teclas **Alt + Tab** .</span><span class="sxs-lookup"><span data-stu-id="c7f2d-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-133">**CursorBlinkRate**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-136">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| \\ \\ \| de escritorio del panel de control de CursorBlinkRate"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-137">Período de tiempo entre parpadeos de cursor sucesivos.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="c7f2d-138">Ejemplo: 530</span><span class="sxs-lookup"><span data-stu-id="c7f2d-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-142">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-142">Textual description of the current object.</span></span>

<span data-ttu-id="c7f2d-143">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c7f2d-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-144">**DragFullWindows**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-147">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry de \| escritorio del panel de control de \\ \\ \| DragFullWindows")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-148">El contenido de una ventana se muestra cuando un usuario mueve la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-149">**GridGranularity**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-152">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| \\ \\ \| de escritorio del panel de control de GridGranularity"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 píxeles")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-153">Espaciado de la cuadrícula a la que se enlazan las ventanas en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="c7f2d-154">Esto facilita la organización de ventanas.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-154">This makes organizing windows easier.</span></span> <span data-ttu-id="c7f2d-155">Normalmente, el espaciado es lo suficientemente bueno como para que el usuario no lo advierta.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="c7f2d-156">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="c7f2d-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-157">**IconSpacing**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-158">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-160">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \\ \\ WindowMetrics \| IconSpacing "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-161">Espaciado entre iconos.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-161">Spacing between icons.</span></span>

<span data-ttu-id="c7f2d-162">Ejemplo: 75</span><span class="sxs-lookup"><span data-stu-id="c7f2d-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-163">**IconTitleFaceName**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-166">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \\ \\ WindowMetrics \| IconFont ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-167">Fuente utilizada para los nombres de los iconos.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="c7f2d-168">Ejemplo: "MS San Serif"</span><span class="sxs-lookup"><span data-stu-id="c7f2d-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-169">**IconTitleSize**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-172">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Font and Text Structures \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-173">Tamaño de fuente del icono.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-173">Icon font size.</span></span>

<span data-ttu-id="c7f2d-174">Ejemplo: 9</span><span class="sxs-lookup"><span data-stu-id="c7f2d-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-175">**IconTitleWrap**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-176">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-178">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \\ \\ WindowMetrics \| IconTitleWrap ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-179">El texto del título del icono se ajusta a la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-180">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-183">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-184">Nombre que identifica el perfil de escritorio actual.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="c7f2d-185">Ejemplo: "MainProf"</span><span class="sxs-lookup"><span data-stu-id="c7f2d-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-186">**Patrón**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-189">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Patrón de escritorio predeterminado del panel de control \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-190">Nombre del patrón que se utiliza como fondo para el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-191">**ScreenSaverActive**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-192">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-194">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \| ScreenSaveActive ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-195">El protector de pantalla está activo.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-196">**ScreenSaverExecutable**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-199">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de Control predeterminadoSCRNSAVE.EXE de \\ \\ escritorio \| ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-200">Nombre del archivo ejecutable del protector de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="c7f2d-201">Ejemplo: "LOGON. SCR</span><span class="sxs-lookup"><span data-stu-id="c7f2d-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-202">**ScreenSaverSecure**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-203">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-205">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \| ScreenSaverIsSecure ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-206">La contraseña está habilitada para el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-207">**ScreenSaverTimeout**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-210">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \| SCREENSAVETIMEOUT "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-211">Cantidad de tiempo que transcurre antes de que se inicie el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-215">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7f2d-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-216">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="c7f2d-217">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c7f2d-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-218">**Fondo de pantalla**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-221">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ \\ \\ Papel tapiz del escritorio del panel de control predeterminado \| ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-222">Nombre de archivo del diseño del papel tapiz en el fondo del escritorio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="c7f2d-223">Ejemplo: "WINNT.BMP"</span><span class="sxs-lookup"><span data-stu-id="c7f2d-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-224">**WallpaperStretched**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-225">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-227">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \| WallpaperStyle ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-228">El papel tapiz se ajusta para rellenar toda la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="c7f2d-229">Microsoft Plus!</span><span class="sxs-lookup"><span data-stu-id="c7f2d-229">Microsoft Plus!</span></span> <span data-ttu-id="c7f2d-230">debe instalarse antes de que esta opción esté disponible.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-230">must be installed before this option is available.</span></span> <span data-ttu-id="c7f2d-231">Si **es false**, el papel tapiz conserva sus dimensiones originales en el fondo del escritorio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2d-232">**WallpaperTiled**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f2d-233">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7f2d-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f2d-235">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Panel de control predeterminado \\ \\ escritorio \| TileWallpaper ")</span><span class="sxs-lookup"><span data-stu-id="c7f2d-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="c7f2d-236">El papel tapiz está en mosaico o centrado.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7f2d-237">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7f2d-237">Remarks</span></span>

<span data-ttu-id="c7f2d-238">La clase de **\_ escritorio Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c7f2d-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="c7f2d-239">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="c7f2d-240">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="c7f2d-241">Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c7f2d-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="c7f2d-242">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7f2d-242">Examples</span></span>

<span data-ttu-id="c7f2d-243">En el ejemplo de código siguiente se describe cómo recuperar información del escritorio.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="c7f2d-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7f2d-244">Requirements</span></span>



| <span data-ttu-id="c7f2d-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7f2d-245">Requirement</span></span> | <span data-ttu-id="c7f2d-246">Value</span><span class="sxs-lookup"><span data-stu-id="c7f2d-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f2d-247">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7f2d-247">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f2d-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7f2d-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7f2d-249">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7f2d-249">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f2d-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7f2d-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7f2d-251">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7f2d-251">Namespace</span></span><br/>                | <span data-ttu-id="c7f2d-252">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c7f2d-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7f2d-253">MOF</span><span class="sxs-lookup"><span data-stu-id="c7f2d-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7f2d-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7f2d-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7f2d-255">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7f2d-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7f2d-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7f2d-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f2d-257">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7f2d-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f2d-258">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c7f2d-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="c7f2d-259">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7f2d-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

