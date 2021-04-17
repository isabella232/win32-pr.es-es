---
description: Recuperar y establecer la información de configuración regional
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recuperar y establecer la información de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686716"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="9fdc1-103">Recuperar y establecer la información de configuración regional</span><span class="sxs-lookup"><span data-stu-id="9fdc1-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="9fdc1-104">La aplicación debe poder recuperar y establecer información específica sobre los [idiomas y configuraciones regionales](locales-and-languages.md)disponibles.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="9fdc1-105">Cada elemento de información de configuración regional, como el nombre de un determinado día de la semana o el carácter que se usa como separador decimal, tiene una constante correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="9fdc1-106">Las constantes disponibles se definen en [constantes de información de configuración regional](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9fdc1-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="9fdc1-107">La aplicación siempre almacena y manipula la información de configuración regional como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="9fdc1-108">No se permiten datos binarios, y los valores numéricos deben especificarse como texto.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="9fdc1-109">Cada tipo de información tiene un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-109">Each type of information has a particular format.</span></span> <span data-ttu-id="9fdc1-110">Además, se vinculan varios tipos juntos para que el cambio de un tipo cambie también el valor del otro tipo.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="9fdc1-111">Para recuperar la información de configuración regional, la aplicación llama a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante que corresponde a la información requerida.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="9fdc1-112">La aplicación puede llamar a [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) para establecer un elemento de información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="9fdc1-113">Aunque es posible que se admita un [identificador de configuración regional](locale-identifiers.md) , no está disponible para su uso por parte de una aplicación a menos que también esté instalada la configuración regional correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="9fdc1-114">Dado que la mayoría de las constantes de información de configuración regional se excluyen mutuamente, solo se puede controlar un tipo de información a la vez.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="9fdc1-115">Las excepciones a esta regla son la [configuración regional \_ use \_ CP \_ ACP](locale-use-cp-acp.md), el número de retorno de la [configuración regional \_ \_ ](locale-return-constants.md)y la [configuración regional \_ NOUSEROVERRIDE](locale-nouseroverride.md), que se pueden combinar con otras constantes mediante un binario o.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="9fdc1-116">No se recomienda el uso de la configuración regional \_ NOUSEROVERRIDE ya que deshabilita las preferencias del usuario.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="9fdc1-117">Al igual que una serie de aplicaciones, por ejemplo Microsoft Active Directory, la aplicación puede mantener sus cadenas en una base de datos ordenable.</span><span class="sxs-lookup"><span data-stu-id="9fdc1-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="9fdc1-118">Para obtener más información, vea [controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9fdc1-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fdc1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fdc1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fdc1-120">Uso de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="9fdc1-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="9fdc1-121">Constantes de información de configuración regional</span><span class="sxs-lookup"><span data-stu-id="9fdc1-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="9fdc1-122">Controlar la ordenación en las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9fdc1-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="9fdc1-123">Trabajar con configuraciones regionales personalizadas</span><span class="sxs-lookup"><span data-stu-id="9fdc1-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 



