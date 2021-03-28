---
description: En esta sección se describe cómo determinar la versión de los archivos dll de Shell en la que se ejecuta la aplicación y cómo dirigirse a la aplicación para una versión específica.
title: 'Versiones de DLL de Shell y Shlwapi '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276736"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="5c12e-103">Versiones de DLL de Shell y Shlwapi </span><span class="sxs-lookup"><span data-stu-id="5c12e-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="5c12e-104">En esta sección se describe cómo determinar la versión de los archivos dll de Shell en la que se ejecuta la aplicación y cómo dirigirse a la aplicación para una versión específica.</span><span class="sxs-lookup"><span data-stu-id="5c12e-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="5c12e-105">Números de versión de DLL</span><span class="sxs-lookup"><span data-stu-id="5c12e-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="5c12e-106">Uso de DllGetVersion para determinar el número de versión</span><span class="sxs-lookup"><span data-stu-id="5c12e-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="5c12e-107">Usar DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="5c12e-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="5c12e-108">Versiones del proyecto</span><span class="sxs-lookup"><span data-stu-id="5c12e-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="5c12e-109">Números de versión de DLL</span><span class="sxs-lookup"><span data-stu-id="5c12e-109">DLL Version Numbers</span></span>

<span data-ttu-id="5c12e-110">Todos los elementos de programación, excepto algunos de los descritos en la documentación de Shell, se encuentran en dos archivos dll: Shell32.dll y Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5c12e-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="5c12e-111">Debido a las mejoras continuas, las diferentes versiones de estos archivos dll implementan características diferentes.</span><span class="sxs-lookup"><span data-stu-id="5c12e-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="5c12e-112">En la documentación de referencia del shell, cada elemento de programación especifica un número de versión de DLL compatible mínimo.</span><span class="sxs-lookup"><span data-stu-id="5c12e-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="5c12e-113">Este número de versión indica que el elemento de programación se implementa en esa versión y versiones posteriores del archivo DLL, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5c12e-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="5c12e-114">Si no se especifica ningún número de versión, el elemento de programación se implementa en todas las versiones existentes de la DLL.</span><span class="sxs-lookup"><span data-stu-id="5c12e-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="5c12e-115">Antes de Windows XP, las nuevas versiones de Shell32.dll y Shlwapi.dll se proporcionaban a veces con nuevas versiones de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5c12e-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="5c12e-116">A partir de Windows XP, esos archivos DLL ya no se proporcionaron como archivos redistribuibles fuera de las nuevas versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c12e-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="5c12e-117">En la tabla siguiente se describen las distintas versiones de DLL y cómo se distribuyeron a Microsoft Internet Explorer 3,0, Windows 95 y Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="5c12e-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="5c12e-118">Shell32.dll versión 4,0 se encuentra en las versiones originales de Windows 95 y Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="5c12e-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="5c12e-119">El shell no se actualizó con la versión 3,0 de Internet Explorer, por lo que Shell32.dll no tiene la versión 4,70.</span><span class="sxs-lookup"><span data-stu-id="5c12e-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="5c12e-120">Shell32.dll versiones 4,71 y 4,72 se enviaron con las correspondientes versiones de Internet Explorer, pero no se instalaron necesariamente (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="5c12e-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="5c12e-121">En el caso de las versiones posteriores a Microsoft Internet Explorer 4,01 y Windows 98, los números de versión de Shell32.dll y Shlwapi.dll divergen.</span><span class="sxs-lookup"><span data-stu-id="5c12e-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="5c12e-122">En general, debe suponer que los archivos dll tienen números de versión diferentes y probar cada uno por separado.</span><span class="sxs-lookup"><span data-stu-id="5c12e-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="5c12e-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="5c12e-123">Shell32.dll</span></span>

| <span data-ttu-id="5c12e-124">Versión</span><span class="sxs-lookup"><span data-stu-id="5c12e-124">Version</span></span> | <span data-ttu-id="5c12e-125">Plataforma de distribución</span><span class="sxs-lookup"><span data-stu-id="5c12e-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5c12e-126">4.0</span><span class="sxs-lookup"><span data-stu-id="5c12e-126">4.0</span></span>     | <span data-ttu-id="5c12e-127">Windows 95 y Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="5c12e-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="5c12e-128">4.71</span><span class="sxs-lookup"><span data-stu-id="5c12e-128">4.71</span></span>    | <span data-ttu-id="5c12e-129">Microsoft Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="5c12e-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="5c12e-130">Vea la nota 1.</span><span class="sxs-lookup"><span data-stu-id="5c12e-130">See note 1.</span></span>                                |
| <span data-ttu-id="5c12e-131">4.72</span><span class="sxs-lookup"><span data-stu-id="5c12e-131">4.72</span></span>    | <span data-ttu-id="5c12e-132">Internet Explorer 4,01 y Windows 98.</span><span class="sxs-lookup"><span data-stu-id="5c12e-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="5c12e-133">Vea la nota 1.</span><span class="sxs-lookup"><span data-stu-id="5c12e-133">See note 1.</span></span>                          |
| <span data-ttu-id="5c12e-134">5.0</span><span class="sxs-lookup"><span data-stu-id="5c12e-134">5.0</span></span>     | <span data-ttu-id="5c12e-135">Windows 2000 y Windows Millennium Edition (Windows me).</span><span class="sxs-lookup"><span data-stu-id="5c12e-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="5c12e-136">Vea la nota 2.</span><span class="sxs-lookup"><span data-stu-id="5c12e-136">See note 2.</span></span>       |
| <span data-ttu-id="5c12e-137">6.0</span><span class="sxs-lookup"><span data-stu-id="5c12e-137">6.0</span></span>     | <span data-ttu-id="5c12e-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c12e-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="5c12e-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="5c12e-139">6.0.1</span></span>   | <span data-ttu-id="5c12e-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c12e-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="5c12e-141">6.1</span><span class="sxs-lookup"><span data-stu-id="5c12e-141">6.1</span></span>     | <span data-ttu-id="5c12e-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c12e-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="5c12e-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="5c12e-143">Shlwapi.dll</span></span>

| <span data-ttu-id="5c12e-144">Versión</span><span class="sxs-lookup"><span data-stu-id="5c12e-144">Version</span></span> | <span data-ttu-id="5c12e-145">Plataforma de distribución</span><span class="sxs-lookup"><span data-stu-id="5c12e-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5c12e-146">4.0</span><span class="sxs-lookup"><span data-stu-id="5c12e-146">4.0</span></span>     | <span data-ttu-id="5c12e-147">Windows 95 y Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="5c12e-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="5c12e-148">4.71</span><span class="sxs-lookup"><span data-stu-id="5c12e-148">4.71</span></span>    | <span data-ttu-id="5c12e-149">Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="5c12e-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="5c12e-150">Vea la nota 1.</span><span class="sxs-lookup"><span data-stu-id="5c12e-150">See note 1.</span></span>                                          |
| <span data-ttu-id="5c12e-151">4.72</span><span class="sxs-lookup"><span data-stu-id="5c12e-151">4.72</span></span>    | <span data-ttu-id="5c12e-152">Internet Explorer 4,01 y Windows 98.</span><span class="sxs-lookup"><span data-stu-id="5c12e-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="5c12e-153">Vea la nota 1.</span><span class="sxs-lookup"><span data-stu-id="5c12e-153">See note 1.</span></span>                          |
| <span data-ttu-id="5c12e-154">4,7</span><span class="sxs-lookup"><span data-stu-id="5c12e-154">4.7</span></span>     | <span data-ttu-id="5c12e-155">Internet Explorer 3. x</span><span class="sxs-lookup"><span data-stu-id="5c12e-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="5c12e-156">5.0</span><span class="sxs-lookup"><span data-stu-id="5c12e-156">5.0</span></span>     | <span data-ttu-id="5c12e-157">Microsoft Internet Explorer 5 y Windows 98 SE.</span><span class="sxs-lookup"><span data-stu-id="5c12e-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="5c12e-158">Vea la nota 2.</span><span class="sxs-lookup"><span data-stu-id="5c12e-158">See note 2.</span></span>                |
| <span data-ttu-id="5c12e-159">5.5</span><span class="sxs-lookup"><span data-stu-id="5c12e-159">5.5</span></span>     | <span data-ttu-id="5c12e-160">Microsoft Internet Explorer 5,5 y Windows Millennium Edition (Windows me)</span><span class="sxs-lookup"><span data-stu-id="5c12e-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="5c12e-161">6.0</span><span class="sxs-lookup"><span data-stu-id="5c12e-161">6.0</span></span>     | <span data-ttu-id="5c12e-162">Windows XP y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c12e-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="5c12e-163">**Nota 1:** Todos los sistemas con Internet Explorer 4,0 o 4,01 tenían la versión asociada de Shlwapi.dll (4,71 o 4,72, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="5c12e-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="5c12e-164">Sin embargo, para sistemas anteriores a Windows 98, se pueden instalar Internet Explorer 4,0 y 4,01 con o sin lo que se conocía como *Shell integrado*.</span><span class="sxs-lookup"><span data-stu-id="5c12e-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="5c12e-165">Si Internet Explorer se instaló con el shell integrado, también se instalará la versión asociada de Shell32.dll (4,71 o 4,72).</span><span class="sxs-lookup"><span data-stu-id="5c12e-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="5c12e-166">Si Internet Explorer se instaló sin el shell integrado, Shell32.dll permaneció como la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="5c12e-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="5c12e-167">En otras palabras, la presencia de la versión 4,71 o 4,72 de Shlwapi.dll en un sistema no garantiza que Shell32.dll tenga el mismo número de versión.</span><span class="sxs-lookup"><span data-stu-id="5c12e-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="5c12e-168">Todos los sistemas de Windows 98 tienen la versión 4,72 de Shell32.dll.</span><span class="sxs-lookup"><span data-stu-id="5c12e-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="5c12e-169">**Nota 2:** La versión 5,0 de Shlwapi.dll se distribuyó con Internet Explorer 5 y se encontró en todos los sistemas en los que se instaló Internet Explorer 5, con la excepción de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5c12e-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="5c12e-170">La versión 5,0 de Shell32.dll se distribuyó de forma nativa con Windows 2000 y Windows Millennium Edition (Windows me), junto con la versión 5,0 de Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5c12e-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="5c12e-171">Uso de DllGetVersion para determinar el número de versión</span><span class="sxs-lookup"><span data-stu-id="5c12e-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="5c12e-172">A partir de la versión 4,71, los archivos dll de Shell, entre otros, empezaron a exportar [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="5c12e-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="5c12e-173">Una aplicación puede llamar a esta función para determinar qué versión de DLL está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5c12e-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="5c12e-174">Los archivos dll no exportan necesariamente [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="5c12e-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="5c12e-175">Pruébelo siempre antes de intentar usarlo.</span><span class="sxs-lookup"><span data-stu-id="5c12e-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="5c12e-176">En las versiones de Windows anteriores a Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) devuelve una estructura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) que contiene los números de versión principal y secundaria, el número de compilación y un identificador de plataforma.</span><span class="sxs-lookup"><span data-stu-id="5c12e-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="5c12e-177">En el caso de los sistemas Windows 2000 y versiones posteriores, es posible que **DllGetVersion** devuelva una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="5c12e-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="5c12e-178">Además de la información proporcionada a través de **DLLVERSIONINFO**, **DLLVERSIONINFO2** también proporciona el número de revisión que identifica la Service Pack instalada más reciente, que proporciona una manera más eficaz de comparar los números de versión.</span><span class="sxs-lookup"><span data-stu-id="5c12e-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="5c12e-179">Dado que el primer miembro de **DLLVERSIONINFO2** es una estructura **DLLVERSIONINFO** , la estructura posterior es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="5c12e-180">Usar DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="5c12e-180">Using DllGetVersion</span></span>

<span data-ttu-id="5c12e-181">La función de ejemplo siguiente `GetVersion` carga un archivo dll especificado e intenta llamar a su función [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="5c12e-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="5c12e-182">Si se realiza correctamente, usa una macro para empaquetar los números de versión principal y secundaria de la estructura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) en un **valor DWORD** que se devuelve a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="5c12e-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="5c12e-183">Si el archivo DLL no exporta **DllGetVersion**, la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5c12e-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="5c12e-184">Con Windows 2000 y sistemas posteriores, puede modificar la función para controlar la posibilidad de que **DllGetVersion** devuelva una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="5c12e-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="5c12e-185">Si es así, use la información del miembro **ullVersion** de la estructura **DLLVERSIONINFO2** para comparar las versiones, los números de compilación y las versiones de Service Pack.</span><span class="sxs-lookup"><span data-stu-id="5c12e-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="5c12e-186">La macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) simplifica la tarea de comparar estos valores con los de **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="5c12e-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="5c12e-187">El uso incorrecto de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="5c12e-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="5c12e-188">Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c12e-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


<span data-ttu-id="5c12e-189">En el ejemplo de código siguiente se muestra cómo puede usar `GetVersion` para comprobar si Shell32.dll es la versión 6,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5c12e-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="5c12e-190">Versiones del proyecto</span><span class="sxs-lookup"><span data-stu-id="5c12e-190">Project Versions</span></span>

<span data-ttu-id="5c12e-191">Para asegurarse de que la aplicación es compatible con las distintas versiones de destino de un archivo. dll, las macros de versión están presentes en los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="5c12e-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="5c12e-192">Estas macros se utilizan para definir, excluir o volver a definir ciertas definiciones para diferentes versiones de la DLL.</span><span class="sxs-lookup"><span data-stu-id="5c12e-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="5c12e-193">Vea [usar los encabezados de Windows](../winprog/using-the-windows-headers.md) para obtener una descripción detallada de estas macros.</span><span class="sxs-lookup"><span data-stu-id="5c12e-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="5c12e-194">Por ejemplo, el nombre de macro **\_ Win32 \_ IE** suele encontrarse en encabezados más antiguos.</span><span class="sxs-lookup"><span data-stu-id="5c12e-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="5c12e-195">Usted es responsable de definir la macro como un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="5c12e-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="5c12e-196">Este número de versión define la versión de destino de la aplicación que está usando el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="5c12e-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="5c12e-197">En la tabla siguiente se muestran los números de versión disponibles y el efecto que cada tiene en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c12e-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="5c12e-198">Versión</span><span class="sxs-lookup"><span data-stu-id="5c12e-198">Version</span></span> | <span data-ttu-id="5c12e-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c12e-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c12e-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="5c12e-200">0x0200</span></span>  | <span data-ttu-id="5c12e-201">La aplicación es compatible con Shell32.dll versión 4,00 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="5c12e-202">La aplicación no puede implementar características que se agregaron después de la versión 4,00.</span><span class="sxs-lookup"><span data-stu-id="5c12e-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="5c12e-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="5c12e-203">0x0300</span></span>  | <span data-ttu-id="5c12e-204">La aplicación es compatible con Shell32.dll versión 4,70 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="5c12e-205">La aplicación no puede implementar características que se agregaron después de la versión 4,70.</span><span class="sxs-lookup"><span data-stu-id="5c12e-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="5c12e-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="5c12e-206">0x0400</span></span>  | <span data-ttu-id="5c12e-207">La aplicación es compatible con Shell32.dll versión 4,71 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="5c12e-208">La aplicación no puede implementar características que se agregaron después de la versión 4,71.</span><span class="sxs-lookup"><span data-stu-id="5c12e-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="5c12e-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="5c12e-209">0x0401</span></span>  | <span data-ttu-id="5c12e-210">La aplicación es compatible con Shell32.dll versión 4,72 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="5c12e-211">La aplicación no puede implementar características que se agregaron después de la versión 4,72.</span><span class="sxs-lookup"><span data-stu-id="5c12e-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="5c12e-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="5c12e-212">0x0500</span></span>  | <span data-ttu-id="5c12e-213">La aplicación es compatible con Shell32.dll y Shlwapi.dll versión 5,0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="5c12e-214">La aplicación no puede implementar características que se agregaron después de la versión 5,0 de Shell32.dll y Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5c12e-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="5c12e-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="5c12e-215">0x0501</span></span>  | <span data-ttu-id="5c12e-216">La aplicación es compatible con Shell32.dll y Shlwapi.dll versión 5,0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="5c12e-217">La aplicación no puede implementar características que se agregaron después de la versión 5,0 de Shell32.dll y Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5c12e-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="5c12e-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="5c12e-218">0x0600</span></span>  | <span data-ttu-id="5c12e-219">La aplicación es compatible con Shell32.dll y Shlwapi.dll versión 6,0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="5c12e-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="5c12e-220">La aplicación no puede implementar características que se agregaron después de la versión 6,0 de Shell32.dll y Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5c12e-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="5c12e-221">Si no define la macro de **\_ \_ IE de Win32** en el proyecto, se define automáticamente como 0x0500.</span><span class="sxs-lookup"><span data-stu-id="5c12e-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="5c12e-222">Para definir un valor diferente, puede agregar lo siguiente a las directivas de compilador en el archivo make; Sustituya el número de versión deseado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="5c12e-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="5c12e-223">Otro método consiste en agregar una línea similar a la siguiente en el código fuente antes de incluir los archivos de encabezado del shell.</span><span class="sxs-lookup"><span data-stu-id="5c12e-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="5c12e-224">Sustituya el número de versión deseado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="5c12e-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
