---
description: '\\Panel de control HKCU \\ escritorio.'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423427"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="c5c25-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="c5c25-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="c5c25-104">**\\Panel de control HKCU \\ escritorio**</span><span class="sxs-lookup"><span data-stu-id="c5c25-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="c5c25-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c5c25-105">Data type</span></span> | <span data-ttu-id="c5c25-106">Intervalo</span><span class="sxs-lookup"><span data-stu-id="c5c25-106">Range</span></span>       | <span data-ttu-id="c5c25-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c5c25-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="c5c25-108">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c5c25-108">REG\_SZ</span></span>   | <span data-ttu-id="c5c25-109">*Nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="c5c25-109">*File name*</span></span> | <span data-ttu-id="c5c25-110">(Ninguna)</span><span class="sxs-lookup"><span data-stu-id="c5c25-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="c5c25-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5c25-111">Description</span></span>

<span data-ttu-id="c5c25-112">Especifica el nombre del archivo ejecutable del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c5c25-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="c5c25-113">Cambiar método</span><span class="sxs-lookup"><span data-stu-id="c5c25-113">Change Method</span></span>

<span data-ttu-id="c5c25-114">Para cambiar el valor de esta entrada, en el panel de control, haga doble clic en **pantalla**, haga clic en la pestaña **protector de pantalla** y, a continuación, seleccione un protector de pantalla de la lista **protector de pantalla** .</span><span class="sxs-lookup"><span data-stu-id="c5c25-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="c5c25-115">También puede cambiar esta entrada con la función de la interfaz de programación de aplicaciones (API) **InstallScreenSaver**, que se exporta mediante Desk.cpl.</span><span class="sxs-lookup"><span data-stu-id="c5c25-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="c5c25-116">Puede tener acceso a esta función con la línea de comandos **rundll32.exe desk.cpl,** *archivo* InstallScreenSaver, donde *archivo* es el nombre de un archivo ejecutable del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c5c25-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="c5c25-117">Método de activación</span><span class="sxs-lookup"><span data-stu-id="c5c25-117">Activation Method</span></span>

<span data-ttu-id="c5c25-118">Los cambios que se realicen en esta entrada entrarán en vigor la próxima vez que el sistema inicie un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c5c25-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="c5c25-119">Los cambios realizados en esta entrada mientras se está ejecutando un protector de pantalla no tienen ningún efecto en el protector de pantalla en ejecución.</span><span class="sxs-lookup"><span data-stu-id="c5c25-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="c5c25-120">Notas</span><span class="sxs-lookup"><span data-stu-id="c5c25-120">Notes</span></span>

-   <span data-ttu-id="c5c25-121">Los sistemas operativos Windows agregan esta entrada al registro cuando se usa **Mostrar** en el panel de control para seleccionar un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c5c25-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="c5c25-122">Si deshabilita todos los protectores de pantalla eligiendo **(ninguno)** en la lista de protectores de pantalla, el sistema operativo elimina esta entrada del registro y llama a la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con *uiAction* igual a SPI \_ SETSCREENSAVEACTIVE y *uiParam* igual a **false**.</span><span class="sxs-lookup"><span data-stu-id="c5c25-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="c5c25-123">Esta entrada se puede sustituir por un valor de directiva de grupo en los sistemas que admiten directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="c5c25-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="c5c25-124">Mientras el **nombre del archivo ejecutable del protector de pantalla** Directiva de grupo está habilitado, el sistema omite esta entrada.</span><span class="sxs-lookup"><span data-stu-id="c5c25-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="c5c25-125">La configuración de esta configuración de Directiva se almacena en la entrada **SCRNSAVE.EXE** , que se encuentra en la subclave de **directivas** .</span><span class="sxs-lookup"><span data-stu-id="c5c25-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
