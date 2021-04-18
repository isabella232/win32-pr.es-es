---
title: Uso de estructuras en WCS 1.0
description: La mayoría de las estructuras utilizadas por WCS 1,0 son muy sencillas y requieren poca explicación. Están documentados en la sección de referencia de WCS 1,0 titulada estructuras.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Sistema de color de Windows (WCS), estructuras
- WCS (sistema de colores de Windows), estructuras
- Administración del color de imagen, estructuras
- Administración del color, estructuras
- colores, estructuras
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721375"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="bdff0-109">Uso de estructuras en WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="bdff0-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="bdff0-110">La mayoría de las estructuras utilizadas por WCS 1,0 son muy sencillas y requieren poca explicación.</span><span class="sxs-lookup"><span data-stu-id="bdff0-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="bdff0-111">Están documentados en la sección de referencia de WCS 1,0 titulada [estructuras](structures.md).</span><span class="sxs-lookup"><span data-stu-id="bdff0-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="bdff0-112">Las excepciones son la estructura [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) que usa la función [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) y las siguientes estructuras de Windows definidas en WinGDI. h:</span><span class="sxs-lookup"><span data-stu-id="bdff0-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="bdff0-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="bdff0-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="bdff0-114">**LOGCOLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="bdff0-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="bdff0-115">**CIEXYZ**</span><span class="sxs-lookup"><span data-stu-id="bdff0-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="bdff0-116">**CIEXYZTRIPLE**</span><span class="sxs-lookup"><span data-stu-id="bdff0-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="bdff0-117">Los temas siguientes se describen con mayor longitud:</span><span class="sxs-lookup"><span data-stu-id="bdff0-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="bdff0-118">Estructuras de encabezado de mapa de bits de Windows</span><span class="sxs-lookup"><span data-stu-id="bdff0-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="bdff0-119">Diferencias entre los encabezados V4 y V5</span><span class="sxs-lookup"><span data-stu-id="bdff0-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="bdff0-120">Bitmap.exe: utilidad de Command-Line para convertir encabezados de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="bdff0-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="bdff0-121">Estructuras de encabezado de mapa de bits de Windows</span><span class="sxs-lookup"><span data-stu-id="bdff0-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="bdff0-122">WCS 1,0 permite vincular o incrustar perfiles de color ICC en mapas de bits independientes del dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="bdff0-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="bdff0-123">Esto permite que los colores DIB se caracterizan de manera más precisa de lo que era posible con WCS en Windows 95.</span><span class="sxs-lookup"><span data-stu-id="bdff0-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="bdff0-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , la nueva estructura de encabezado de mapa de bits, se define en WinGDI. h en la versión de Windows 98.</span><span class="sxs-lookup"><span data-stu-id="bdff0-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="bdff0-125">Para fines de desarrollo, también se incluye en el archivo ICM. h con la referencia de este programador.</span><span class="sxs-lookup"><span data-stu-id="bdff0-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="bdff0-126">La estructura **BITMAPV5HEADER** es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="bdff0-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="bdff0-127">El miembro **bV5CSType** puede tener el perfil de valores \_ incrustado o el perfil \_ vinculado para especificar si un perfil está incrustado o vinculado con el Dib.</span><span class="sxs-lookup"><span data-stu-id="bdff0-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="bdff0-128">El miembro **bV5ProfileData** es el desplazamiento en bytes desde el principio de la estructura **BITMAPV5HEADER** hasta el inicio de los datos del perfil.</span><span class="sxs-lookup"><span data-stu-id="bdff0-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="bdff0-129">Si el perfil está incrustado, los datos del perfil son el perfil real y, si está vinculado, los datos del perfil son el nombre de archivo terminado en NULL del perfil.</span><span class="sxs-lookup"><span data-stu-id="bdff0-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="bdff0-130">No puede ser una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="bdff0-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="bdff0-131">Debe estar compuesto exclusivamente por caracteres del juego de caracteres de Windows (página de códigos 1252).</span><span class="sxs-lookup"><span data-stu-id="bdff0-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="bdff0-132">Cuando se carga un DIB en la memoria, los datos del perfil (si están presentes) deben seguir la tabla de colores y **bV5ProfileData** deben proporcionar el desplazamiento de los datos de perfil desde el principio de la estructura **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="bdff0-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="bdff0-133">El valor de este miembro será diferente ahora, ya que los bits de mapa de bits no siguen la tabla de colores en memoria.</span><span class="sxs-lookup"><span data-stu-id="bdff0-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="bdff0-134">Las aplicaciones deben modificar el miembro **bV5ProfileData** después de cargar el DIB en la memoria.</span><span class="sxs-lookup"><span data-stu-id="bdff0-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="bdff0-135">En el caso de los archivos DIB empaquetados, los datos del perfil deben seguir los bits de mapa de bits similares al formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="bdff0-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="bdff0-136">El miembro **bV5ProfileData** todavía debe proporcionar el desplazamiento de los datos de perfil desde el principio de la estructura **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="bdff0-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="bdff0-137">Las aplicaciones deben tener acceso a los datos del perfil solo cuando **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** está integrado en el perfil \_ o se vincula el perfil \_ .</span><span class="sxs-lookup"><span data-stu-id="bdff0-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="bdff0-138">Si un perfil está vinculado, la ruta de acceso del perfil puede ser cualquier nombre completo (incluida una ruta de acceso de red) que se puede abrir mediante la función **CreateFile** de Win32.</span><span class="sxs-lookup"><span data-stu-id="bdff0-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="bdff0-139">Diferencias entre los encabezados V4 y V5</span><span class="sxs-lookup"><span data-stu-id="bdff0-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="bdff0-140">Al trabajar con la nueva estructura de mapa de bits, resulta útil reconocer las diferencias en el modo en que se configuran las estructuras **BITMAPV4HEADER** y **BITMAPV5HEADER** :</span><span class="sxs-lookup"><span data-stu-id="bdff0-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="bdff0-141">Encabezado V4</span><span class="sxs-lookup"><span data-stu-id="bdff0-141">V4 Header</span></span>     | <span data-ttu-id="bdff0-142">Significado</span><span class="sxs-lookup"><span data-stu-id="bdff0-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdff0-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-143">**bV4CSType**</span></span> | <span data-ttu-id="bdff0-144">\_RGB calibrado por LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="bdff0-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="bdff0-145">Este valor implica que los extremos y las gamma se proporcionan en los campos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="bdff0-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="bdff0-146">Los valores fantasma causan problemas.</span><span class="sxs-lookup"><span data-stu-id="bdff0-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="bdff0-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-147">**bV4CSType**</span></span> | <span data-ttu-id="bdff0-148">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="bdff0-148">LCS\_sRGB.</span></span> <span data-ttu-id="bdff0-149">Este valor implica que el mapa de bits está en el espacio de colores sRGB (se omiten las gamma y los puntos de conexión).</span><span class="sxs-lookup"><span data-stu-id="bdff0-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="bdff0-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-150">**bV4CSType**</span></span> | <span data-ttu-id="bdff0-151">espacio de colores de Windows de LCS \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bdff0-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="bdff0-152">Este valor implica que el mapa de bits está en el espacio de colores predeterminado de Windows.</span><span class="sxs-lookup"><span data-stu-id="bdff0-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="bdff0-153">Encabezado V5</span><span class="sxs-lookup"><span data-stu-id="bdff0-153">V5 Header</span></span>     | <span data-ttu-id="bdff0-154">Significado</span><span class="sxs-lookup"><span data-stu-id="bdff0-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdff0-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-155">**bV5CSType**</span></span> | <span data-ttu-id="bdff0-156">\_RGB calibrado por LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="bdff0-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="bdff0-157">Este valor implica que los extremos y las gamma se proporcionan en los campos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="bdff0-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="bdff0-158">Los valores fantasma causan problemas.</span><span class="sxs-lookup"><span data-stu-id="bdff0-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="bdff0-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-159">**bV5CSType**</span></span> | <span data-ttu-id="bdff0-160">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="bdff0-160">LCS\_sRGB.</span></span> <span data-ttu-id="bdff0-161">Este valor implica que el mapa de bits está en el espacio de colores sRGB (se omiten las gamma y los puntos de conexión).</span><span class="sxs-lookup"><span data-stu-id="bdff0-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="bdff0-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-162">**bV5CSType**</span></span> | <span data-ttu-id="bdff0-163">Perfil \_ incrustado.</span><span class="sxs-lookup"><span data-stu-id="bdff0-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="bdff0-164">Este valor implica que **bV5ProfileData** señala a un búfer de memoria que contiene el perfil que se va a usar (las gamma y los puntos de conexión se omiten).</span><span class="sxs-lookup"><span data-stu-id="bdff0-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="bdff0-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-165">**bV5CSType**</span></span> | <span data-ttu-id="bdff0-166">Perfil \_ vinculado.</span><span class="sxs-lookup"><span data-stu-id="bdff0-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="bdff0-167">Este valor implica que **bV5ProfileData** apunta al nombre de archivo del perfil que se va a usar (se omiten las gamma y los puntos de conexión).</span><span class="sxs-lookup"><span data-stu-id="bdff0-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="bdff0-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="bdff0-168">**bV5CSType**</span></span> | <span data-ttu-id="bdff0-169">espacio de colores de Windows de LCS \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bdff0-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="bdff0-170">Este valor implica que el mapa de bits está en el espacio de colores predeterminado de Windows.</span><span class="sxs-lookup"><span data-stu-id="bdff0-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="bdff0-171">Para convertir mapas de bits anteriores a y desde la nueva estructura **BITMAPV5HEADER** , se incluye un archivo de utilidad de conversión de línea de comandos denominado Bitmap.exe en la referencia del programador de WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="bdff0-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="bdff0-172">BitMap.exe: utilidad de Command-Line para convertir encabezados de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="bdff0-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="bdff0-173">Bitmap.exe es una utilidad de línea de comandos ubicada en la \\ carpeta bin debajo de la carpeta de instalación que especificó.</span><span class="sxs-lookup"><span data-stu-id="bdff0-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="bdff0-174">Modifica los encabezados de los mapas de bits de Windows, lo que permite convertir los mapas de bits existentes de las estructuras de encabezado **BITMAPINFOHEADER** y **BITMAPV4HEADER** en la estructura **BITMAPV5HEADER** más reciente y volver de nuevo.</span><span class="sxs-lookup"><span data-stu-id="bdff0-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="bdff0-175">La sintaxis de la línea de comandos es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="bdff0-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="bdff0-176">Los modificadores de la línea de comandos tienen los siguientes efectos.</span><span class="sxs-lookup"><span data-stu-id="bdff0-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="bdff0-177">Conmutador</span><span class="sxs-lookup"><span data-stu-id="bdff0-177">Switch</span></span> | <span data-ttu-id="bdff0-178">Significado</span><span class="sxs-lookup"><span data-stu-id="bdff0-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="bdff0-179">/d</span><span class="sxs-lookup"><span data-stu-id="bdff0-179">/d</span></span>     | <span data-ttu-id="bdff0-180">Los valores predeterminados se especifican automáticamente en los encabezados convertidos.</span><span class="sxs-lookup"><span data-stu-id="bdff0-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="bdff0-181">/1</span><span class="sxs-lookup"><span data-stu-id="bdff0-181">/1</span></span>     | <span data-ttu-id="bdff0-182">Convertir los mapas de bits especificados en **BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="bdff0-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="bdff0-183">/4</span><span class="sxs-lookup"><span data-stu-id="bdff0-183">/4</span></span>     | <span data-ttu-id="bdff0-184">Convertir los mapas de bits especificados en **BITMAPV4HEADER**</span><span class="sxs-lookup"><span data-stu-id="bdff0-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="bdff0-185">/5</span><span class="sxs-lookup"><span data-stu-id="bdff0-185">/5</span></span>     | <span data-ttu-id="bdff0-186">Convertir los mapas de bits especificados en **BITMAPV5HEADER**</span><span class="sxs-lookup"><span data-stu-id="bdff0-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="bdff0-187">/f</span><span class="sxs-lookup"><span data-stu-id="bdff0-187">/f</span></span>     | <span data-ttu-id="bdff0-188">Fuerza la conversión, incluso si el mapa de bits ya tiene el encabezado derecho</span><span class="sxs-lookup"><span data-stu-id="bdff0-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="bdff0-189">/s</span><span class="sxs-lookup"><span data-stu-id="bdff0-189">/s</span></span>     | <span data-ttu-id="bdff0-190">Convierte los mapas de bits de la carpeta especificada y todos sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="bdff0-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 