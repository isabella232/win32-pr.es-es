---
title: Analizar excepciones
description: La API del servidor HTTP proporciona claves del registro para admitir el análisis de excepciones a la especificación HTTP/1.1 por compatibilidad con versiones anteriores.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analizar excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994336"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="e0497-104">Analizar excepciones</span><span class="sxs-lookup"><span data-stu-id="e0497-104">Parsing Exceptions</span></span>

<span data-ttu-id="e0497-105">La API del servidor HTTP proporciona claves del registro para admitir el análisis de excepciones a la especificación HTTP/1.1 por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e0497-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="e0497-106">Estas excepciones no están habilitadas de forma predeterminada y solo deben habilitarse en caso de que el servidor experimente problemas de compatibilidad con clientes HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0497-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="e0497-107">Estos valores se crean en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="e0497-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="e0497-108">En la tabla siguiente se enumeran las claves del registro proporcionadas para admitir las excepciones que se muestran.</span><span class="sxs-lookup"><span data-stu-id="e0497-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="e0497-109">Para habilitar una excepción, establezca el valor de clave correspondiente en 1 y reinicie el servicio HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0497-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="e0497-110">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="e0497-110">Key name</span></span>                              | <span data-ttu-id="e0497-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0497-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0497-112">AllowWeakHeaderNameSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="e0497-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="e0497-113">Permite que el analizador HTTP acepte nombres de encabezado con caracteres separadores como '? '.</span><span class="sxs-lookup"><span data-stu-id="e0497-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e0497-114">AllowWeakHeaderValueSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="e0497-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="e0497-115">Permite que el analizador HTTP acepte valores de encabezado con caracteres de control sin formato (sin escape).</span><span class="sxs-lookup"><span data-stu-id="e0497-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e0497-116">AllowCaseInsensitiveVerbs (DWORD)</span><span class="sxs-lookup"><span data-stu-id="e0497-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="e0497-117">Permite que el analizador HTTP acepte métodos o verbos HTTP en minúsculas, como "Get".</span><span class="sxs-lookup"><span data-stu-id="e0497-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e0497-118">AllowUnEscapedRestrictedChars (DWORD)</span><span class="sxs-lookup"><span data-stu-id="e0497-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="e0497-119">Permite que el analizador HTTP acepte caracteres de control en abspath y cadenas de consulta de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e0497-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="e0497-120">En el caso de una dirección URL absoluta, no se permitirán caracteres de control en el nombre de host.</span><span class="sxs-lookup"><span data-stu-id="e0497-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="e0497-121">Todos los tipos de direcciones URL, es decir, UTF8, DBCS y ANSI, permitirán caracteres de control.</span><span class="sxs-lookup"><span data-stu-id="e0497-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="e0497-122">Se permitirán todos los caracteres de control ASCII excepto NUL (0x00), LF (0x0a), CR (0x0d) y horizontal (0x09).</span><span class="sxs-lookup"><span data-stu-id="e0497-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




