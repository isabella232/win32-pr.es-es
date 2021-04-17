---
description: Un identificador de idioma es una abreviatura numérica internacional estándar para el idioma de un país o región geográfica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificadores de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666595"
---
# <a name="language-identifiers"></a><span data-ttu-id="45c95-103">Identificadores de idioma</span><span class="sxs-lookup"><span data-stu-id="45c95-103">Language Identifiers</span></span>

<span data-ttu-id="45c95-104">Un identificador de idioma es una abreviatura numérica internacional estándar para el [idioma](locales-and-languages.md) de un país o región geográfica.</span><span class="sxs-lookup"><span data-stu-id="45c95-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="45c95-105">Cada idioma tiene un identificador de idioma único (tipo de datos LANGID), un valor de 16 bits que consta de un identificador de idioma principal y un identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="45c95-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="45c95-106">Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](language-identifier-constants-and-strings.md).</span><span class="sxs-lookup"><span data-stu-id="45c95-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="45c95-107">Un identificador de idioma se construye mediante la macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) .</span><span class="sxs-lookup"><span data-stu-id="45c95-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="45c95-108">En la ilustración siguiente se muestra el formato de los bits en un identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="45c95-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="45c95-109">Estos son los identificadores de idioma predefinidos:</span><span class="sxs-lookup"><span data-stu-id="45c95-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="45c95-110">IDIOMA \_ predeterminado del sistema \_ .</span><span class="sxs-lookup"><span data-stu-id="45c95-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="45c95-111">Idioma predeterminado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="45c95-111">The operating system default language.</span></span>
-   <span data-ttu-id="45c95-112">\_valor predeterminado de usuario de Lang \_ .</span><span class="sxs-lookup"><span data-stu-id="45c95-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="45c95-113">El idioma del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="45c95-113">The language of the current user.</span></span>

<span data-ttu-id="45c95-114">La aplicación puede recuperar los identificadores de idioma actuales mediante las funciones de la [interfaz de usuario multilingüe](multilingual-user-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="45c95-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45c95-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45c95-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c95-116">Configuraciones regionales e idiomas</span><span class="sxs-lookup"><span data-stu-id="45c95-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="45c95-117">Constantes y cadenas de identificador de idioma</span><span class="sxs-lookup"><span data-stu-id="45c95-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="45c95-118">Interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="45c95-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="45c95-119">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="45c95-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



