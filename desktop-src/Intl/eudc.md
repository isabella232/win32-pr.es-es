---
description: La clave del Registro EUDC contiene una o varias subclaves que contienen valores que definen las fuentes asociadas a caracteres definidos por el usuario final (EUDC) para una página de códigos determinada.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120710"
---
# <a name="eudc"></a><span data-ttu-id="b48ee-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="b48ee-103">EUDC</span></span>

<span data-ttu-id="b48ee-104">La clave del Registro EUDC contiene una o varias subclaves que contienen valores que definen las fuentes asociadas a caracteres definidos por el usuario final [(EUDC)](end-user-defined-characters.md) para una página de códigos determinada.</span><span class="sxs-lookup"><span data-stu-id="b48ee-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="b48ee-105">Tiene la siguiente ubicación del Registro:</span><span class="sxs-lookup"><span data-stu-id="b48ee-105">It has the following registry location:</span></span>

<span data-ttu-id="b48ee-106">HKEY \_ CURRENT \_ USER \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="b48ee-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="b48ee-107">El formato es:</span><span class="sxs-lookup"><span data-stu-id="b48ee-107">The format is:</span></span>

<span data-ttu-id="b48ee-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="b48ee-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="b48ee-109">donde:</span><span class="sxs-lookup"><span data-stu-id="b48ee-109">where:</span></span>



| <span data-ttu-id="b48ee-110">Value</span><span class="sxs-lookup"><span data-stu-id="b48ee-110">Value</span></span>                         | <span data-ttu-id="b48ee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b48ee-111">Description</span></span>                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48ee-112">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="b48ee-112">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="b48ee-113">Nombre predefinido usado para establecer la fuente predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="b48ee-113">Predefined name used to set the system default font.</span></span> <span data-ttu-id="b48ee-114">No hay ninguna fuente EUDC predeterminada del sistema a menos que se especifique explícitamente esta entrada.</span><span class="sxs-lookup"><span data-stu-id="b48ee-114">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="b48ee-115">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="b48ee-115">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="b48ee-116">Nombre definido por el usuario asociado a una fuente TrueType que no sea EUDC.</span><span class="sxs-lookup"><span data-stu-id="b48ee-116">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="b48ee-117">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="b48ee-117">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="b48ee-118">Cadena que consta del nombre de archivo de un archivo de fuente EUDC independiente.</span><span class="sxs-lookup"><span data-stu-id="b48ee-118">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="b48ee-119">Este archivo identifica una fuente que se va a asociar a TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="b48ee-119">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="b48ee-120">En el ejemplo siguiente se muestra la clave EUDC para la página de códigos 932.</span><span class="sxs-lookup"><span data-stu-id="b48ee-120">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="b48ee-121">En el ejemplo siguiente se establece la fuente EUDC predeterminada del sistema como Eudc.ttf y se asocian las fuentes EUDC independientes Mineudc.ttf y Goteudc.ttf con los nombres de fuente MS Mincho y MS Deserción, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b48ee-121">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="b48ee-122">Cuando la página de códigos de Windows (ACP del sistema) asociada al idioma de los programas no Unicode coincide con la subclave, el subsistema GDI busca los pares de valores de subclave para obtener información de visualización sobre el carácter.</span><span class="sxs-lookup"><span data-stu-id="b48ee-122">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="b48ee-123">Primero busca un nombre que coincida con la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="b48ee-123">It first looks for a name matching the current font.</span></span> <span data-ttu-id="b48ee-124">Si no hay ninguno, examina el valor SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="b48ee-124">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="b48ee-125">Si no se define ningún valor, GDI trata el carácter como indefinido.</span><span class="sxs-lookup"><span data-stu-id="b48ee-125">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="b48ee-126">Tenga en cuenta que el propio texto no tiene que estar en la página de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="b48ee-126">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="b48ee-127">Por ejemplo, suponga que la página de códigos tiene el identificador 1252, la página de códigos predeterminada de Windows para inglés.</span><span class="sxs-lookup"><span data-stu-id="b48ee-127">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="b48ee-128">Una aplicación pasa el único punto de código Unicode U+E000, en el área de uso privado (PUA) unicode, [**a DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="b48ee-128">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="b48ee-129">En este caso, GDI examina los valores del Registro en 1252 para obtener la información de fuente de las propiedades de visualización de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b48ee-129">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b48ee-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b48ee-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b48ee-131">Entradas del Registro eudc</span><span class="sxs-lookup"><span data-stu-id="b48ee-131">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="b48ee-132">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="b48ee-132">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
