---
description: Use esta anotación para definir el contenido de un archivo externo como el valor de inicialización de un parámetro de efecto.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Anotación de inicialización de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274646"
---
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="91ffd-103">Anotación de inicialización de parámetros</span><span class="sxs-lookup"><span data-stu-id="91ffd-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="91ffd-104">Use esta anotación para definir el contenido de un archivo externo como el valor de inicialización de un parámetro de efecto.</span><span class="sxs-lookup"><span data-stu-id="91ffd-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="91ffd-105">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91ffd-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="91ffd-106">donde value es una cadena de texto ASCII que puede contener una ruta de acceso absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="91ffd-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="91ffd-107">Una ruta de acceso relativa es relativa al directorio que contiene el archivo de efecto.</span><span class="sxs-lookup"><span data-stu-id="91ffd-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="91ffd-108">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91ffd-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="91ffd-109">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="91ffd-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91ffd-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91ffd-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ffd-111">Referencia de las anotaciones y semánticas estándar de DirectX</span><span class="sxs-lookup"><span data-stu-id="91ffd-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



