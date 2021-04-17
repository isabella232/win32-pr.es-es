---
title: Atributo src (VMLFrame) (VML)
description: Atributo src (VMLFrame) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359093"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="e432c-103">Atributo src (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="e432c-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="e432c-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e432c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e432c-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="e432c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e432c-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="e432c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e432c-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="e432c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e432c-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e432c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e432c-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e432c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e432c-110">Define el origen de datos para el marco.</span><span class="sxs-lookup"><span data-stu-id="e432c-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="e432c-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e432c-111">Read/write.</span></span> <span data-ttu-id="e432c-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="e432c-112">**String**.</span></span>

<span data-ttu-id="e432c-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="e432c-113">**Applies To**</span></span>

[<span data-ttu-id="e432c-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="e432c-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="e432c-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="e432c-115">**Tag Syntax**</span></span>

<span data-ttu-id="e432c-116"><v: *elemento* src = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="e432c-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="e432c-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="e432c-117">**Script Syntax**</span></span>

<span data-ttu-id="e432c-118">*Element* . src = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="e432c-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="e432c-119">*expresión* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="e432c-119">*expression*=*element*.src</span></span>

<span data-ttu-id="e432c-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="e432c-120">**Remarks**</span></span>

<span data-ttu-id="e432c-121">El atributo **src** puede incluir las siguientes sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e432c-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="e432c-122">Dirección URL del archivo externo.</span><span class="sxs-lookup"><span data-stu-id="e432c-122">URL to external file.</span></span> <span data-ttu-id="e432c-123">El archivo debe ser un archivo XML con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="e432c-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="e432c-124">En el archivo, debe tener una o varias formas de VML con identificadores válidos a los que se pueda hacer referencia mediante esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e432c-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="e432c-125">En la siguiente referencia, los archivos externos tienen la extensión. VML, pero se puede usar cualquier extensión:</span><span class="sxs-lookup"><span data-stu-id="e432c-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="e432c-126">Puede hacer referencia a una forma en el mismo archivo utilizando la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="e432c-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="e432c-127">Si **clip** es **false**, la forma se escalará para ajustarse al marco.</span><span class="sxs-lookup"><span data-stu-id="e432c-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="e432c-128">Si **es true**, no se mostrarán las partes de la forma que estén fuera del marco.</span><span class="sxs-lookup"><span data-stu-id="e432c-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="e432c-129">Tenga en cuenta que el [origen](origin-attribute--vmlframe--vml.md) y [el tamaño](size-attribute--vmlframe.md) no se usarán a menos que el **recorte** sea **true**.</span><span class="sxs-lookup"><span data-stu-id="e432c-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="e432c-130">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="e432c-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="e432c-131">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e432c-131">**Example**</span></span>

<span data-ttu-id="e432c-132">Se recortará la imagen definida en el archivo externo.</span><span class="sxs-lookup"><span data-stu-id="e432c-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 