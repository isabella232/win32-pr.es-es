---
title: LANGUAGE (instrucción)
description: Define el idioma de todos los recursos hasta la siguiente instrucción de lenguaje o hasta el final del archivo.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menús de instrucciones de lenguaje y otros recursos
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533166"
---
# <a name="language-statement"></a><span data-ttu-id="bedf5-104">LANGUAGE (instrucción)</span><span class="sxs-lookup"><span data-stu-id="bedf5-104">LANGUAGE statement</span></span>

<span data-ttu-id="bedf5-105">Define el idioma de todos los recursos hasta la siguiente instrucción de **lenguaje** o hasta el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="bedf5-105">Defines the language for all resources up to the next **LANGUAGE** statement or to the end of the file.</span></span>

<span data-ttu-id="bedf5-106">Cuando la instrucción del **lenguaje** aparece antes del principio del cuerpo de una definición de recursos [**Accelerators**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**stringtable**](stringtable-resource.md) , el idioma especificado solo se aplica a ese recurso.</span><span class="sxs-lookup"><span data-stu-id="bedf5-106">When the **LANGUAGE** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition, the specified language applies only to that resource.</span></span>

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span data-ttu-id="bedf5-107"><span id="language"></span><span id="LANGUAGE"></span>*módulo*</span><span class="sxs-lookup"><span data-stu-id="bedf5-107"><span id="language"></span><span id="LANGUAGE"></span>*language*</span></span>
</dt> <dd>

<span data-ttu-id="bedf5-108">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="bedf5-108">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bedf5-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*subidioma*</span><span class="sxs-lookup"><span data-stu-id="bedf5-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*</span></span>
</dt> <dd>

<span data-ttu-id="bedf5-110">Identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="bedf5-110">Sublanguage identifier.</span></span>

</dd> </dl>

<span data-ttu-id="bedf5-111">Para obtener más información, vea [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="bedf5-111">For more information, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="see-also"></a><span data-ttu-id="bedf5-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="bedf5-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bedf5-113">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="bedf5-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="bedf5-114">**SUS**</span><span class="sxs-lookup"><span data-stu-id="bedf5-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="bedf5-115">**MENU**</span><span class="sxs-lookup"><span data-stu-id="bedf5-115">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="bedf5-116">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="bedf5-116">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="bedf5-117">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="bedf5-117">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="bedf5-118">**Versión**</span><span class="sxs-lookup"><span data-stu-id="bedf5-118">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 