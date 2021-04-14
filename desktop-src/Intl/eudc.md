---
description: La clave del registro EUDC contiene una o más subclaves que contienen valores que definen las fuentes asociadas a los caracteres definidos por el usuario final (EUDCs) de una página de códigos determinada.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668411"
---
# <a name="eudc"></a><span data-ttu-id="6c625-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="6c625-103">EUDC</span></span>

<span data-ttu-id="6c625-104">La clave del registro EUDC contiene una o más subclaves que contienen valores que definen las fuentes asociadas a los [caracteres definidos por el usuario final (EUDCs)](end-user-defined-characters.md) de una página de códigos determinada.</span><span class="sxs-lookup"><span data-stu-id="6c625-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="6c625-105">Tiene la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="6c625-105">It has the following registry location:</span></span>

<span data-ttu-id="6c625-106">HKEY \_ Current \_ User \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="6c625-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="6c625-107">El formato es:</span><span class="sxs-lookup"><span data-stu-id="6c625-107">The format is:</span></span>

<span data-ttu-id="6c625-108">EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="6c625-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="6c625-109">donde:</span><span class="sxs-lookup"><span data-stu-id="6c625-109">where:</span></span>



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c625-110">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="6c625-110">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="6c625-111">Nombre predefinido que se usa para establecer la fuente predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="6c625-111">Predefined name used to set the system default font.</span></span> <span data-ttu-id="6c625-112">No hay ninguna fuente EUDC predeterminada del sistema, a menos que se especifique explícitamente esta entrada.</span><span class="sxs-lookup"><span data-stu-id="6c625-112">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="6c625-113">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="6c625-113">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="6c625-114">Nombre definido por el usuario asociado a una fuente TrueType que no es EUDC.</span><span class="sxs-lookup"><span data-stu-id="6c625-114">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="6c625-115">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="6c625-115">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="6c625-116">Cadena formada por el nombre de archivo de un archivo de fuente EUDC independiente.</span><span class="sxs-lookup"><span data-stu-id="6c625-116">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="6c625-117">Este archivo identifica una fuente que se va a asociar a TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="6c625-117">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="6c625-118">En el ejemplo siguiente se muestra la clave EUDC para la página de códigos 932.</span><span class="sxs-lookup"><span data-stu-id="6c625-118">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="6c625-119">En el ejemplo siguiente se establece la fuente EUDC predeterminada del sistema como EUDC. ttf y se asocian las fuentes EUDC independientes Mineudc. ttf y Goteudc. ttf con los nombres de fuente MS Mincho y MS Gothic, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6c625-119">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="6c625-120">Cuando la página de códigos de Windows (sistema ACP) asociada con el idioma para programas no Unicode coincide con la subclave, el subsistema GDI busca los pares de valores de subclave para obtener información sobre el carácter.</span><span class="sxs-lookup"><span data-stu-id="6c625-120">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="6c625-121">Primero busca un nombre que coincida con la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="6c625-121">It first looks for a name matching the current font.</span></span> <span data-ttu-id="6c625-122">Si no hay ninguno, examina el valor de SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="6c625-122">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="6c625-123">Si no se define ningún valor, GDI trata el carácter como sin definir.</span><span class="sxs-lookup"><span data-stu-id="6c625-123">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="6c625-124">Tenga en cuenta que el texto no tiene que estar en la página de códigos de Windows.</span><span class="sxs-lookup"><span data-stu-id="6c625-124">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="6c625-125">Por ejemplo, supongamos que la página de códigos tiene el identificador 1252, la página de códigos predeterminada de Windows para inglés.</span><span class="sxs-lookup"><span data-stu-id="6c625-125">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="6c625-126">Una aplicación pasa a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)el punto de código Unicode U + E000 y, en el área de uso privado de Unicode (PUA).</span><span class="sxs-lookup"><span data-stu-id="6c625-126">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="6c625-127">En este caso, GDI examina los valores del registro en 1252 para obtener la información de fuente de las propiedades de presentación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6c625-127">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c625-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c625-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c625-129">Entradas del registro de EUDC</span><span class="sxs-lookup"><span data-stu-id="6c625-129">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="6c625-130">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="6c625-130">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
