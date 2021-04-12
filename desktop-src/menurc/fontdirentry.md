---
title: Estructura FONTDIRENTRY
description: Contiene información sobre una fuente individual de un grupo de recursos de fuentes. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menús de la estructura FONTDIRENTRY y otros recursos
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489664"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="ada5c-105">Estructura FONTDIRENTRY</span><span class="sxs-lookup"><span data-stu-id="ada5c-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="ada5c-106">Contiene información sobre una fuente individual de un grupo de recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="ada5c-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="ada5c-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="ada5c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada5c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ada5c-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="ada5c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ada5c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ada5c-110">**dfVersion**</span><span class="sxs-lookup"><span data-stu-id="ada5c-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-112">Un número de versión definido por el usuario para los datos de recursos que las herramientas pueden utilizar para leer y escribir archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="ada5c-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-113">**dfSize**</span><span class="sxs-lookup"><span data-stu-id="ada5c-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ada5c-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-115">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ada5c-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-116">**dfCopyright \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="ada5c-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-117">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="ada5c-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-118">La información de copyright del proveedor de fuentes.</span><span class="sxs-lookup"><span data-stu-id="ada5c-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-119">**dfType**</span><span class="sxs-lookup"><span data-stu-id="ada5c-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-120">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-121">El tipo de archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-122">**dfPoints**</span><span class="sxs-lookup"><span data-stu-id="ada5c-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-123">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-124">Tamaño de punto en el que este juego de caracteres tiene un aspecto óptimo.</span><span class="sxs-lookup"><span data-stu-id="ada5c-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-125">**dfVertRes**</span><span class="sxs-lookup"><span data-stu-id="ada5c-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-126">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-127">Resolución vertical, en puntos por pulgada, a la que se ha digitalizado este juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ada5c-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-128">**dfHorizRes**</span><span class="sxs-lookup"><span data-stu-id="ada5c-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-129">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-130">Resolución horizontal, en puntos por pulgada, a la que se ha digitalizado este juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ada5c-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-131">**dfAscent**</span><span class="sxs-lookup"><span data-stu-id="ada5c-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-132">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-133">Distancia desde la parte superior de una celda de definición de caracteres a la línea base de la fuente tipográfica.</span><span class="sxs-lookup"><span data-stu-id="ada5c-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-134">**dfInternalLeading**</span><span class="sxs-lookup"><span data-stu-id="ada5c-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-135">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-136">La cantidad de espacio que se encuentra dentro de los límites establecidos por el miembro **dfPixHeight** .</span><span class="sxs-lookup"><span data-stu-id="ada5c-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="ada5c-137">En esta área pueden aparecer marcas de acento y otros caracteres diacríticos.</span><span class="sxs-lookup"><span data-stu-id="ada5c-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-138">**dfExternalLeading**</span><span class="sxs-lookup"><span data-stu-id="ada5c-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-139">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-140">La cantidad de espacio adicional que la aplicación agrega entre las filas.</span><span class="sxs-lookup"><span data-stu-id="ada5c-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-141">**dfItalic**</span><span class="sxs-lookup"><span data-stu-id="ada5c-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-142">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-143">Fuente en cursiva si no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="ada5c-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-144">**dfUnderline**</span><span class="sxs-lookup"><span data-stu-id="ada5c-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-145">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-146">Fuente subrayada si no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="ada5c-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-147">**dfStrikeOut**</span><span class="sxs-lookup"><span data-stu-id="ada5c-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-148">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-149">Una fuente de tachado si no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="ada5c-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-150">**dfWeight**</span><span class="sxs-lookup"><span data-stu-id="ada5c-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-151">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-152">Peso de la fuente en el intervalo comprendido entre 0 y 1000.</span><span class="sxs-lookup"><span data-stu-id="ada5c-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="ada5c-153">Por ejemplo, 400 es romano y 700 está en negrita.</span><span class="sxs-lookup"><span data-stu-id="ada5c-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="ada5c-154">Si este valor es cero, se usa una ponderación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ada5c-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="ada5c-155">Para obtener más valores definidos, vea la descripción de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="ada5c-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-156">**dfCharSet**</span><span class="sxs-lookup"><span data-stu-id="ada5c-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-157">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-158">Juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-158">The character set of the font.</span></span> <span data-ttu-id="ada5c-159">Para los valores predefinidos, vea la descripción de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="ada5c-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-160">**dfPixWidth**</span><span class="sxs-lookup"><span data-stu-id="ada5c-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-161">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-162">Ancho de la cuadrícula en la que se ha digitalizado una fuente de vector.</span><span class="sxs-lookup"><span data-stu-id="ada5c-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="ada5c-163">En el caso de las fuentes de trama, si el miembro no es igual a cero, representa el ancho de todos los caracteres del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="ada5c-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="ada5c-164">Si el miembro es igual a cero, la fuente tiene caracteres de ancho variable.</span><span class="sxs-lookup"><span data-stu-id="ada5c-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-165">**dfPixHeight**</span><span class="sxs-lookup"><span data-stu-id="ada5c-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-166">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-167">Alto del mapa de bits de caracteres para las fuentes de tramas o el alto de la cuadrícula en la que se ha digitalizado una fuente de vector.</span><span class="sxs-lookup"><span data-stu-id="ada5c-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-168">**dfPitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="ada5c-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-169">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-170">El paso y la familia de la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-170">The pitch and the family of the font.</span></span> <span data-ttu-id="ada5c-171">Para obtener más información, vea la descripción de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="ada5c-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-172">**dfAvgWidth**</span><span class="sxs-lookup"><span data-stu-id="ada5c-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-173">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-174">Ancho medio de los caracteres de la fuente (generalmente definido como el ancho de la letra x).</span><span class="sxs-lookup"><span data-stu-id="ada5c-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="ada5c-175">Este valor no incluye el saliente necesario para los caracteres en negrita o cursiva.</span><span class="sxs-lookup"><span data-stu-id="ada5c-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-176">**dfMaxWidth**</span><span class="sxs-lookup"><span data-stu-id="ada5c-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-177">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-178">El ancho del carácter más ancho de la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-179">**dfFirstChar**</span><span class="sxs-lookup"><span data-stu-id="ada5c-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-180">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-181">El primer código de carácter definido en la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-182">**dfLastChar**</span><span class="sxs-lookup"><span data-stu-id="ada5c-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-183">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-184">El último código de carácter definido en la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-185">**dfDefaultChar**</span><span class="sxs-lookup"><span data-stu-id="ada5c-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-186">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-187">Carácter que se va a sustituir para los caracteres que no están en la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-188">**dfBreakChar**</span><span class="sxs-lookup"><span data-stu-id="ada5c-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-189">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="ada5c-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-190">Carácter que se usará para definir saltos de palabras para la justificación del texto.</span><span class="sxs-lookup"><span data-stu-id="ada5c-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-191">**dfWidthBytes**</span><span class="sxs-lookup"><span data-stu-id="ada5c-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-192">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ada5c-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-193">Número de bytes de cada fila del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="ada5c-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="ada5c-194">Este valor siempre es par que las filas se inicien en los límites de palabras.</span><span class="sxs-lookup"><span data-stu-id="ada5c-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="ada5c-195">En el caso de las fuentes de Vector, este miembro no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="ada5c-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-196">**dfDevice**</span><span class="sxs-lookup"><span data-stu-id="ada5c-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-197">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ada5c-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-198">El desplazamiento en el archivo en una cadena terminada en null que especifica un nombre de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ada5c-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="ada5c-199">En el caso de una fuente genérica, este valor es cero.</span><span class="sxs-lookup"><span data-stu-id="ada5c-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-200">**dfFace**</span><span class="sxs-lookup"><span data-stu-id="ada5c-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-201">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ada5c-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-202">Desplazamiento del archivo en una cadena terminada en null que nombra el tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="ada5c-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-203">**dfReserved**</span><span class="sxs-lookup"><span data-stu-id="ada5c-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-204">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ada5c-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-205">Este miembro está reservado.</span><span class="sxs-lookup"><span data-stu-id="ada5c-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-206">**szDeviceName**</span><span class="sxs-lookup"><span data-stu-id="ada5c-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-207">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="ada5c-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-208">El nombre del dispositivo si este archivo de fuente se designa para un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="ada5c-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="ada5c-209">**szFaceName**</span><span class="sxs-lookup"><span data-stu-id="ada5c-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="ada5c-210">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="ada5c-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="ada5c-211">Nombre del tipo de letra de la fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ada5c-212">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ada5c-212">Remarks</span></span>

<span data-ttu-id="ada5c-213">Hay una estructura **FONTDIRENTRY** para cada fuente del archivo. res.</span><span class="sxs-lookup"><span data-stu-id="ada5c-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="ada5c-214">Las aplicaciones que generan archivos. res con recursos de fuente también deben agregar al archivo una estructura **FONTDIRENTRY** para cada fuente.</span><span class="sxs-lookup"><span data-stu-id="ada5c-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="ada5c-215">Las declaraciones de fuente se pueden mezclar con otras declaraciones de recursos en. Archivo RC porque no es necesario que las fuentes sean contiguas en el archivo. res.</span><span class="sxs-lookup"><span data-stu-id="ada5c-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada5c-216">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ada5c-216">Requirements</span></span>



| <span data-ttu-id="ada5c-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada5c-217">Requirement</span></span> | <span data-ttu-id="ada5c-218">Value</span><span class="sxs-lookup"><span data-stu-id="ada5c-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ada5c-219">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ada5c-219">Minimum supported client</span></span><br/> | <span data-ttu-id="ada5c-220">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ada5c-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ada5c-221">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ada5c-221">Minimum supported server</span></span><br/> | <span data-ttu-id="ada5c-222">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ada5c-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ada5c-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="ada5c-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="ada5c-224">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ada5c-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ada5c-225">**ARRENDAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="ada5c-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="ada5c-226">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="ada5c-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="ada5c-227">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ada5c-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ada5c-228">Recursos</span><span class="sxs-lookup"><span data-stu-id="ada5c-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="ada5c-229">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="ada5c-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ada5c-230">**NDPTECGDI**</span><span class="sxs-lookup"><span data-stu-id="ada5c-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

