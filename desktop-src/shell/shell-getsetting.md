---
description: Recupera una configuración de Shell global.
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Método Shell. GetSetting (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: df87c0c99129a8ececa3c25321a192e25c71c07e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909885"
---
# <a name="shellgetsetting-method"></a><span data-ttu-id="c8bfc-103">Shell. GetSetting (método)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-103">Shell.GetSetting method</span></span>

<span data-ttu-id="c8bfc-104">Recupera una configuración de Shell global.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bfc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8bfc-105">Syntax</span></span>


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="c8bfc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8bfc-107">*lSetting* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8bfc-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bfc-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="c8bfc-108">Type: **long**</span></span>

<span data-ttu-id="c8bfc-109">Valor que especifica la configuración de Shell actual que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="c8bfc-110">Solo se puede recuperar una configuración en cada llamada.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="c8bfc-111">Este método reconoce los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="c8bfc-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-113">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-113">**Windows Vista and later**.</span></span> <span data-ttu-id="c8bfc-114">El estado de las **casillas de verificación para seleccionar elementos** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="c8bfc-115">Esta opción se habilita automáticamente cuando el sistema tiene configurado un dispositivo de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="c8bfc-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="c8bfc-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-119">El estado de la opción **permitir todos los nombres en mayúsculas** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="c8bfc-120">A partir de Windows Vista, esta opción de carpeta ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="c8bfc-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-122">El estado de la opción de hacer **doble clic para abrir un elemento (un solo clic para seleccionar)** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="c8bfc-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTRAr** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="c8bfc-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="c8bfc-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-128">El estado de la visualización del icono en la vista de lista del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="c8bfc-129">Si esta opción está activa, no se muestra ningún icono en la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="c8bfc-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-131">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-131">**Windows Vista and later**.</span></span> <span data-ttu-id="c8bfc-132">El estado del nombre para mostrar se muestra en la vista de lista del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="c8bfc-133">Si esta opción está activa, los iconos se muestran en la vista de lista, pero no los nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="c8bfc-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-135">El estado del **botón Mostrar unidad de red de mapa en la barra de herramientas** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="c8bfc-136">A partir de Windows Vista, esta opción ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="c8bfc-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-138">El estado de la opción del cuadro de **diálogo de confirmación de eliminación** de la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="c8bfc-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-140">El estado de la opción **Buscar automáticamente carpetas e impresoras de red** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="c8bfc-141">A partir de Windows Vista, esta opción ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="c8bfc-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-143">El estado de las **ventanas de la carpeta de inicio en una opción de proceso independiente** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="c8bfc-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-145">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="c8bfc-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-147">El estado de la opción **archivos y carpetas ocultos** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="c8bfc-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-149">El estado de la opción **Mostrar atributos de archivo en la vista de detalle** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="c8bfc-150">A partir de Windows Vista, esta opción ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="c8bfc-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-152">El estado de la opción **Mostrar en color los archivos NTFS cifrados o comprimidos** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="c8bfc-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-154">El estado de la opción **Ocultar extensiones para tipos de archivo conocidos** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="c8bfc-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-156">El estado de la opción **Mostrar Descripción emergente para los elementos de la carpeta y el escritorio** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="c8bfc-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-158">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="c8bfc-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-160">El estado de la opción **Ocultar archivos protegidos del sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="c8bfc-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-162">El estado de la opción **archivos y carpetas ocultos** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="c8bfc-163">En Windows Vista y versiones posteriores, es equivalente a SSF \_ SHOWALLOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="c8bfc-164">En las versiones de Windows anteriores a Windows Vista, este valor hacía referencia al estado de la opción no **Mostrar archivos y carpetas ocultos** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="c8bfc-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-166">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-166">**Windows Vista and later**.</span></span> <span data-ttu-id="c8bfc-167">Estado del icono de **archivo para mostrar en las miniaturas** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="c8bfc-168">Si esta opción está activa, se aplica una superposición de tipo de archivo cuando un archivo proporciona una representación en miniatura.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="c8bfc-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-170">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="c8bfc-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-172">El estado de la opción de visualización de Windows XP, que selecciona entre el estilo de Windows XP y el estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="c8bfc-173">A partir de Windows Vista, esta opción ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="c8bfc-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-175">El estado de la **presentación como una opción de vista Web**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="c8bfc-176">A partir de Windows Vista, esta opción ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="c8bfc-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="c8bfc-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="c8bfc-178">Estado de la opción de **estilo clásico** .</span><span class="sxs-lookup"><span data-stu-id="c8bfc-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="c8bfc-179">A partir de Windows Vista, esta opción ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8bfc-180">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8bfc-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c8bfc-181">JScript</span><span class="sxs-lookup"><span data-stu-id="c8bfc-181">JScript</span></span>

<span data-ttu-id="c8bfc-182">Tipo: \**variante \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="c8bfc-182">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="c8bfc-183">Establézcalo en _ *true*\* si existe la configuración; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-183">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c8bfc-184">VB</span><span class="sxs-lookup"><span data-stu-id="c8bfc-184">VB</span></span>

<span data-ttu-id="c8bfc-185">Tipo: \**variante \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="c8bfc-185">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="c8bfc-186">Establézcalo en _ *true*\* si existe la configuración; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-186">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="c8bfc-187">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c8bfc-187">Examples</span></span>

<span data-ttu-id="c8bfc-188">En los siguientes ejemplos se muestra el uso de **GetSetting** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c8bfc-189">JScript.net</span><span class="sxs-lookup"><span data-stu-id="c8bfc-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="c8bfc-190">VBScript</span><span class="sxs-lookup"><span data-stu-id="c8bfc-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
```



<span data-ttu-id="c8bfc-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c8bfc-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c8bfc-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8bfc-192">Requirements</span></span>



| <span data-ttu-id="c8bfc-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bfc-193">Requirement</span></span> | <span data-ttu-id="c8bfc-194">Value</span><span class="sxs-lookup"><span data-stu-id="c8bfc-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bfc-195">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8bfc-195">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bfc-196">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c8bfc-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c8bfc-197">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8bfc-197">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bfc-198">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8bfc-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c8bfc-199">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8bfc-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8bfc-200"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8bfc-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c8bfc-201">IDL</span><span class="sxs-lookup"><span data-stu-id="c8bfc-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8bfc-202"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8bfc-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c8bfc-203">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8bfc-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8bfc-204"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c8bfc-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




