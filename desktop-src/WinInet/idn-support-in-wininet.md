---
title: Compatibilidad con IDN en WinINet
description: A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL de Unicode se convierte en el nombre de dominio internacionalizado (IDN).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421277"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="1734c-103">Compatibilidad con IDN en WinINet</span><span class="sxs-lookup"><span data-stu-id="1734c-103">IDN Support in WinINet</span></span>

<span data-ttu-id="1734c-104">A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL de Unicode se convierte en el nombre de dominio internacionalizado (IDN).</span><span class="sxs-lookup"><span data-stu-id="1734c-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="1734c-105">Las configuraciones establecidas por la aplicación también pueden modificar partes independientes de la codificación de la dirección URL de Unicode.</span><span class="sxs-lookup"><span data-stu-id="1734c-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="1734c-106">Las versiones ANSI de la API WinINet continúan enviando la dirección URL a través de la conexión tal como la escribe la aplicación; sin embargo, las versiones de WinINet Unicode de la API ahora se ajustan al estándar IDN (RFC3490) para las codificaciones de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="1734c-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="1734c-107">De forma predeterminada, cuando se especifica una dirección URL como un parámetro Unicode, la parte del host, para conexiones proxy y directas, se convierte al formato IDN.</span><span class="sxs-lookup"><span data-stu-id="1734c-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="1734c-108">La aplicación tiene la opción de deshabilitar el formato de host de IDN estableciendo la opción de **Internet \_ \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="1734c-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="1734c-109">La conversión de host de IDN solo se puede habilitar en las conexiones directas o de proxy mediante las marcas de **Internet \_ marca \_ IDN \_ Direct** o de **\_ \_ \_ proxy IDN de marca** de Internet con la **opción de Internet \_ \_ IDN**.</span><span class="sxs-lookup"><span data-stu-id="1734c-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="1734c-110">En el ejemplo de código siguiente se muestra cómo deshabilitar la conversión de host IDN para conexiones proxy y directas.</span><span class="sxs-lookup"><span data-stu-id="1734c-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="1734c-111">Si el formato de host de IDN está deshabilitado, la aplicación tiene la opción de especificar la página de códigos deseada mediante la **\_ Página de \_ códigos** de la opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="1734c-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="1734c-112">En el ejemplo de código siguiente se muestra cómo especificar la página de códigos japonesa.</span><span class="sxs-lookup"><span data-stu-id="1734c-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="1734c-113">La parte de la ruta de acceso de la dirección URL está codificada de forma predeterminada y el resto de los segmentos de la dirección URL, la consulta o el fragmento, se convierten en la página de códigos predeterminada del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="1734c-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="1734c-114">En el ejemplo siguiente se muestra cómo especificar la página de códigos del idioma coreano para la parte de la ruta de acceso de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1734c-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="1734c-115">En la tabla siguiente se definen las opciones que admiten IDN.</span><span class="sxs-lookup"><span data-stu-id="1734c-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="1734c-116">Para obtener más información, vea el tema [Option Flags](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="1734c-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="1734c-117">Opción</span><span class="sxs-lookup"><span data-stu-id="1734c-117">Option</span></span>                            | <span data-ttu-id="1734c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="1734c-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1734c-119">Página de códigos de la opción de INTERNET \_ \_</span><span class="sxs-lookup"><span data-stu-id="1734c-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="1734c-120">Esta opción se establece en la solicitud o en el identificador de conexión para especificar un esquema de codificación de página de códigos para la parte del host de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1734c-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="1734c-121">Esta opción se omite si se habilita IDN.</span><span class="sxs-lookup"><span data-stu-id="1734c-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="1734c-122">\_ruta de \_ acceso de página de la opción de Internet \_</span><span class="sxs-lookup"><span data-stu-id="1734c-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="1734c-123">Esta opción se establece en la solicitud, o el identificador de conexión habilita el esquema de codificación especificado para la parte de la ruta de acceso de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1734c-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="1734c-124">De forma predeterminada, la parte de la ruta de acceso de la dirección URL está codificada en UTF8.</span><span class="sxs-lookup"><span data-stu-id="1734c-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="1734c-125">Página de códigos de opciones de INTERNET \_ \_ \_ extra</span><span class="sxs-lookup"><span data-stu-id="1734c-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="1734c-126">Al establecer esta opción en la solicitud o el identificador de conexión, se habilita el esquema de codificación especificado para la parte adicional de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1734c-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="1734c-127">De forma predeterminada, la parte adicional de la dirección URL se codifica en la página de códigos predeterminada del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="1734c-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="1734c-128">Opciones de INTERNET \_ \_ IDN</span><span class="sxs-lookup"><span data-stu-id="1734c-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="1734c-129">Esta opción se puede usar en la solicitud o el identificador de conexión para habilitar o deshabilitar la conversión de host de IDN.</span><span class="sxs-lookup"><span data-stu-id="1734c-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="1734c-130">Cuando se deshabilita IDN, WinINet utiliza la página de códigos predeterminada del sistema para codificar la parte de host o de autoridad de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1734c-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="1734c-131">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="1734c-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="1734c-132">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="1734c-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="1734c-133">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="1734c-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 