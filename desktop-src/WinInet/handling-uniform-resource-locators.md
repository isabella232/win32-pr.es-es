---
title: Controlar localizadores uniformes de recursos
description: Un localizador uniforme de recursos (URL) es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104558833"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="49b10-103">Controlar localizadores uniformes de recursos</span><span class="sxs-lookup"><span data-stu-id="49b10-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="49b10-104">Un localizador uniforme de recursos (URL) es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet.</span><span class="sxs-lookup"><span data-stu-id="49b10-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="49b10-105">Cada dirección URL está compuesta de un esquema (HTTP, HTTPS o FTP) y una cadena específica del esquema.</span><span class="sxs-lookup"><span data-stu-id="49b10-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="49b10-106">Esta cadena también puede incluir una combinación de una ruta de acceso de directorio, una cadena de búsqueda o un nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="49b10-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="49b10-107">Las funciones WinINet proporcionan la capacidad de crear, combinar, desglosar y canonizar las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="49b10-108">Para obtener más información sobre las direcciones URL, consulte [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) en localizadores de recursos uniformes (URL).</span><span class="sxs-lookup"><span data-stu-id="49b10-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="49b10-109">Las funciones URL operan en una manera orientada a tareas.</span><span class="sxs-lookup"><span data-stu-id="49b10-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="49b10-110">No se comprueba el contenido y el formato de la dirección URL que se proporciona a la función.</span><span class="sxs-lookup"><span data-stu-id="49b10-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="49b10-111">La aplicación que realiza la llamada debe realizar un seguimiento del uso de estas funciones para asegurarse de que los datos están en el formato previsto.</span><span class="sxs-lookup"><span data-stu-id="49b10-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="49b10-112">Por ejemplo, la función [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) convertiría el carácter "%" en la secuencia de escape "%25" cuando no se usaran marcas.</span><span class="sxs-lookup"><span data-stu-id="49b10-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="49b10-113">Si se usa [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) en la dirección URL con formato canónico, la secuencia de escape "%25" se convertiría en la secuencia de escape "%2525", que no funcionaría correctamente.</span><span class="sxs-lookup"><span data-stu-id="49b10-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="49b10-114">¿Qué es una dirección URL con formato canónico?</span><span class="sxs-lookup"><span data-stu-id="49b10-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="49b10-115">Usar las funciones WinINet para controlar las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="49b10-116">Canonicalización de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="49b10-117">Combinación de direcciones URL base y relativas</span><span class="sxs-lookup"><span data-stu-id="49b10-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="49b10-118">Averiguando direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="49b10-119">Creación de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="49b10-120">Acceso directo a las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="49b10-121">¿Qué es una dirección URL con formato canónico?</span><span class="sxs-lookup"><span data-stu-id="49b10-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="49b10-122">El formato de todas las direcciones URL debe seguir la sintaxis y la semántica aceptadas para obtener acceso a los recursos a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="49b10-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="49b10-123">La canonización es el proceso de dar formato a una dirección URL para seguir esta sintaxis y semántica aceptadas.</span><span class="sxs-lookup"><span data-stu-id="49b10-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="49b10-124">Entre los caracteres que se deben codificar se incluyen los caracteres que no tengan ningún carácter gráfico correspondiente en el juego de caracteres codificados por ASCII (hexadecimal 80-FF). que no se usan en el juego de caracteres codificados de US-ASCII, y hexadecimal 00-1F y 7F, que son caracteres de control, espacios en blanco, "%" (que se usa para codificar otros caracteres) y caracteres no seguros (<, >, ", \# , {,}, \| , \\ , ^, ~,, \[ \] y ').</span><span class="sxs-lookup"><span data-stu-id="49b10-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="49b10-125">Usar las funciones WinINet para controlar las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="49b10-126">En la tabla siguiente se resumen las funciones de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="49b10-127">Función</span><span class="sxs-lookup"><span data-stu-id="49b10-127">Function</span></span>                                                   | <span data-ttu-id="49b10-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="49b10-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="49b10-129">**InternetCanonicalizeUrl**</span><span class="sxs-lookup"><span data-stu-id="49b10-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="49b10-130">Canonicalizes la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="49b10-131">**InternetCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="49b10-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="49b10-132">Combina direcciones URL base y relativas.</span><span class="sxs-lookup"><span data-stu-id="49b10-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="49b10-133">**InternetCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="49b10-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="49b10-134">Analiza una cadena de dirección URL en componentes.</span><span class="sxs-lookup"><span data-stu-id="49b10-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="49b10-135">**InternetCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="49b10-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="49b10-136">Crea una cadena de dirección URL a partir de componentes.</span><span class="sxs-lookup"><span data-stu-id="49b10-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="49b10-137">**InternetOpenUrl**</span><span class="sxs-lookup"><span data-stu-id="49b10-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="49b10-138">Comienza a recuperar un recurso FTP, HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="49b10-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="49b10-139">Canonicalización de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-139">Canonicalizing URLs</span></span>

<span data-ttu-id="49b10-140">La canonicalización de una dirección URL es el proceso que convierte una dirección URL, que puede contener caracteres no seguros como espacios en blanco, caracteres reservados, etc., en un formato aceptado.</span><span class="sxs-lookup"><span data-stu-id="49b10-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="49b10-141">La función [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) se puede usar para canonizar las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="49b10-142">Esta función está muy orientada a tareas, por lo que la aplicación debe realizar un seguimiento de su uso con cuidado.</span><span class="sxs-lookup"><span data-stu-id="49b10-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="49b10-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) no comprueba si la dirección URL que se le ha pasado ya está en formato canónico y que la dirección URL que devuelve es válida.</span><span class="sxs-lookup"><span data-stu-id="49b10-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="49b10-144">Las cinco marcas siguientes controlan cómo [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) controla una dirección URL determinada.</span><span class="sxs-lookup"><span data-stu-id="49b10-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="49b10-145">Las marcas se pueden usar en combinación.</span><span class="sxs-lookup"><span data-stu-id="49b10-145">The flags can be used in combination.</span></span> <span data-ttu-id="49b10-146">Si no se usa ninguna marca, la función codifica la dirección URL de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49b10-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="49b10-147">Value</span><span class="sxs-lookup"><span data-stu-id="49b10-147">Value</span></span>                     | <span data-ttu-id="49b10-148">Significado</span><span class="sxs-lookup"><span data-stu-id="49b10-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b10-149">\_modo de explorador ICU \_</span><span class="sxs-lookup"><span data-stu-id="49b10-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="49b10-150">No codifique ni descodifique caracteres después de " \# " o "?", y no quite los espacios en blanco finales después de "?".</span><span class="sxs-lookup"><span data-stu-id="49b10-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="49b10-151">Si no se especifica este valor, se codifica la dirección URL completa y se quita el espacio en blanco final.</span><span class="sxs-lookup"><span data-stu-id="49b10-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="49b10-152">descodificación de ICU \_</span><span class="sxs-lookup"><span data-stu-id="49b10-152">ICU\_DECODE</span></span>               | <span data-ttu-id="49b10-153">Convierta todas las secuencias de% XX en caracteres, incluidas las secuencias de escape, antes de analizar la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="49b10-154">\_ \_ solo espacios de codificación de ICU \_</span><span class="sxs-lookup"><span data-stu-id="49b10-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="49b10-155">Codificar solo los espacios.</span><span class="sxs-lookup"><span data-stu-id="49b10-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="49b10-156">ICU \_ no \_ codificar</span><span class="sxs-lookup"><span data-stu-id="49b10-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="49b10-157">No convierta caracteres no seguros en secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="49b10-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="49b10-158">ICU \_ no \_ meta</span><span class="sxs-lookup"><span data-stu-id="49b10-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="49b10-159">No quite las secuencias meta (como "." y "..") de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="49b10-160">La \_ marca de descodificación de ICU solo debe usarse en direcciones URL con formato canónico, porque supone que todas las secuencias de% XX son códigos de escape y las convierte en los caracteres indicados por el código.</span><span class="sxs-lookup"><span data-stu-id="49b10-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="49b10-161">Si la dirección URL tiene un símbolo "%" que no forma parte de un código de escape, la \_ DEScodificación de ICU todavía la trata como una.</span><span class="sxs-lookup"><span data-stu-id="49b10-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="49b10-162">Esta característica puede hacer que [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) cree una dirección URL no válida.</span><span class="sxs-lookup"><span data-stu-id="49b10-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="49b10-163">Para usar [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) para devolver una dirección URL completamente descodificada, \_ \_ se deben especificar las marcas de codificación de ICU y de no codificar \_ .</span><span class="sxs-lookup"><span data-stu-id="49b10-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="49b10-164">Este programa de instalación supone que la dirección URL que se pasa a [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) se ha canónico previamente.</span><span class="sxs-lookup"><span data-stu-id="49b10-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="49b10-165">Combinación de direcciones URL base y relativas</span><span class="sxs-lookup"><span data-stu-id="49b10-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="49b10-166">Una dirección URL relativa es una representación compacta de la ubicación de un recurso con respecto a una dirección URL base absoluta.</span><span class="sxs-lookup"><span data-stu-id="49b10-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="49b10-167">El analizador debe conocer la dirección URL base y normalmente incluye el esquema, la ubicación de red y las partes de la ruta de acceso de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="49b10-168">Una aplicación puede llamar a [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) para combinar la dirección URL relativa con su dirección URL base.</span><span class="sxs-lookup"><span data-stu-id="49b10-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="49b10-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) también canonicalizes la dirección URL resultante.</span><span class="sxs-lookup"><span data-stu-id="49b10-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="49b10-170">Averiguando direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-170">Cracking URLs</span></span>

<span data-ttu-id="49b10-171">La función [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) separa una dirección URL en sus partes componentes y devuelve los componentes indicados por la estructura de [**\_ componentes URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) que se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="49b10-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="49b10-172">Los componentes que componen la estructura de los [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) son el número de esquema, el nombre de host, el número de puerto, el nombre de usuario, la contraseña, la ruta de acceso de dirección URL e información adicional (como los parámetros de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="49b10-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="49b10-173">Cada componente, excepto el esquema y los números de puerto, tiene un miembro de cadena que contiene la información y un miembro que contiene la longitud del miembro de cadena.</span><span class="sxs-lookup"><span data-stu-id="49b10-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="49b10-174">El esquema y los números de Puerto solo tienen un miembro que almacena el valor correspondiente. ambos se devuelven en todas las llamadas correctas a [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span><span class="sxs-lookup"><span data-stu-id="49b10-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="49b10-175">Para obtener el valor de un componente determinado en la estructura de [**\_ los componentes URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , el miembro que almacena la longitud de cadena de ese componente debe establecerse en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="49b10-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="49b10-176">El miembro de cadena puede ser la dirección de un búfer o un **valor null**.</span><span class="sxs-lookup"><span data-stu-id="49b10-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="49b10-177">Si el miembro de puntero contiene la dirección de un búfer, el miembro de longitud de cadena debe contener el tamaño de dicho búfer.</span><span class="sxs-lookup"><span data-stu-id="49b10-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="49b10-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) devuelve la información del componente como una cadena en el búfer y almacena la longitud de la cadena en el miembro de longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="49b10-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="49b10-179">Si el miembro de puntero es **null**, el miembro de longitud de cadena se puede establecer en cualquier valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="49b10-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="49b10-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) almacena la dirección del primer carácter de la cadena de dirección URL que contiene la información del componente y establece la longitud de la cadena en el número de caracteres de la parte restante de la cadena de dirección URL que pertenece al componente.</span><span class="sxs-lookup"><span data-stu-id="49b10-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="49b10-181">Todos los miembros de puntero se establecen en **null** con un punto de miembro de longitud distinto de cero en el punto de inicio adecuado en la cadena de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="49b10-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="49b10-182">La longitud almacenada en el miembro de longitud debe usarse para determinar el final de la información del componente individual.</span><span class="sxs-lookup"><span data-stu-id="49b10-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="49b10-183">Para finalizar la inicialización correcta de la estructura de los [**\_ componentes URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , el miembro **dwStructSize** debe establecerse en el tamaño de la estructura de [**\_ componentes URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , en bytes.</span><span class="sxs-lookup"><span data-stu-id="49b10-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="49b10-184">En el ejemplo siguiente se devuelven los componentes de la dirección URL en el cuadro de edición, IDC \_ PreOpen1, y se devuelven los componentes al cuadro de lista, IDC \_ PreOpenList.</span><span class="sxs-lookup"><span data-stu-id="49b10-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="49b10-185">Para mostrar solo la información de un componente individual, esta función copia el carácter inmediatamente después de la información del componente en la cadena y lo reemplaza temporalmente por un **valor null**.</span><span class="sxs-lookup"><span data-stu-id="49b10-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="49b10-186">Creación de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-186">Creating URLs</span></span>

<span data-ttu-id="49b10-187">La función [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) usa la información de la estructura de [**\_ componentes URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) para crear un localizador uniforme de recursos.</span><span class="sxs-lookup"><span data-stu-id="49b10-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="49b10-188">Los componentes que componen la estructura de los [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) son el esquema, el nombre de host, el número de puerto, el nombre de usuario, la contraseña, la ruta de acceso de dirección URL e información adicional (como los parámetros de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="49b10-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="49b10-189">Cada componente, excepto el número de puerto, tiene un miembro de cadena que contiene la información y un miembro que contiene la longitud del miembro de cadena.</span><span class="sxs-lookup"><span data-stu-id="49b10-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="49b10-190">Para cada componente necesario, el miembro de puntero debe contener la dirección del búfer que contiene la información.</span><span class="sxs-lookup"><span data-stu-id="49b10-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="49b10-191">El miembro de longitud debe establecerse en cero si el miembro de puntero contiene la dirección de una cadena terminada en cero; el miembro de longitud debe establecerse en la longitud de cadena si el miembro de puntero contiene la dirección de una cadena que no termina en cero.</span><span class="sxs-lookup"><span data-stu-id="49b10-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="49b10-192">El miembro de puntero de cualquier componente que no sea necesario debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="49b10-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="49b10-193">Acceso directo a las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="49b10-193">Accessing URLs Directly</span></span>

<span data-ttu-id="49b10-194">Se puede tener acceso a los recursos FTP y HTTP en Internet directamente mediante las funciones [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)y [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="49b10-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="49b10-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) abre una conexión al recurso en la dirección URL pasada a la función.</span><span class="sxs-lookup"><span data-stu-id="49b10-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="49b10-196">Cuando se establece esta conexión, hay dos pasos posibles.</span><span class="sxs-lookup"><span data-stu-id="49b10-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="49b10-197">En primer lugar, si el recurso es un archivo, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) puede descargarlo; en segundo lugar, si el recurso es un directorio, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) puede enumerar los archivos dentro del directorio (excepto cuando se usan servidores proxy CERN).</span><span class="sxs-lookup"><span data-stu-id="49b10-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="49b10-198">Para obtener más información sobre [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), consulte [lectura de archivos](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="49b10-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="49b10-199">Para obtener más información sobre [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consulte [Buscar el siguiente archivo](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="49b10-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="49b10-200">En el caso de las aplicaciones que necesitan funcionar a través de un proxy CERN, se puede usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para tener acceso a los archivos y directorios FTP.</span><span class="sxs-lookup"><span data-stu-id="49b10-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="49b10-201">Las solicitudes de FTP se empaquetan para aparecer como una solicitud HTTP, que el proxy de CERN aceptaría.</span><span class="sxs-lookup"><span data-stu-id="49b10-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="49b10-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) y la dirección URL del recurso.</span><span class="sxs-lookup"><span data-stu-id="49b10-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="49b10-203">La dirección URL debe incluir el esquema (http:, FTP:, archivo: \[ para un archivo local \] o https: \[ para el protocolo de hipertexto seguro \] ) y la ubicación de red (por ejemplo, `www.microsoft.com` ).</span><span class="sxs-lookup"><span data-stu-id="49b10-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="49b10-204">La dirección URL también puede incluir una ruta de acceso (por ejemplo,/ISAPI/gomscom.asp? TARGET =/Windows/Feature/) y el nombre del recurso (por ejemplo, default.htm).</span><span class="sxs-lookup"><span data-stu-id="49b10-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="49b10-205">En el caso de las solicitudes HTTP o HTTPS, se pueden incluir encabezados adicionales.</span><span class="sxs-lookup"><span data-stu-id="49b10-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="49b10-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)y [**INTERNETSETFILEPOINTER**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo direcciones URL http o https) pueden usar el identificador creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para descargar el recurso.</span><span class="sxs-lookup"><span data-stu-id="49b10-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="49b10-207">En el diagrama siguiente se muestran los identificadores que se van a usar con cada función.</span><span class="sxs-lookup"><span data-stu-id="49b10-207">The following diagram illustrates which handles to use with each function.</span></span>

![identificadores para usar con funciones](images/ax-wnt02.png)

<span data-ttu-id="49b10-209">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)usa el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) raíz creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="49b10-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="49b10-210">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (no se muestra aquí) y [**INTERNETSETFILEPOINTER**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo direcciones URL http o https) pueden usar el identificador de **HINTERNET** creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="49b10-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="49b10-211">Para obtener más información, vea [**identificadores de HINTERNET**](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="49b10-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="49b10-212">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="49b10-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="49b10-213">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="49b10-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="49b10-214">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="49b10-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 