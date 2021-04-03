---
title: Estructura XML del archivo de definición de máscara
description: Estructura XML del archivo de definición de máscara
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- crear máscaras, archivos de definición de máscara
- Aspectos de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, estructura XML
- Estructura XML para los archivos de definición de máscara
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075988"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="b2db4-109">Estructura XML del archivo de definición de máscara</span><span class="sxs-lookup"><span data-stu-id="b2db4-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="b2db4-110">El archivo de definición de máscara se escribe en XML.</span><span class="sxs-lookup"><span data-stu-id="b2db4-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="b2db4-111">Una de las características importantes de XML es que está completamente estructurada y es similar a un esquema.</span><span class="sxs-lookup"><span data-stu-id="b2db4-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="b2db4-112">El código XML simplemente es una serie de elementos como **View** y **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b2db4-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="b2db4-113">Empezará con los elementos y, a continuación, los definirá con atributos.</span><span class="sxs-lookup"><span data-stu-id="b2db4-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="b2db4-114">En el resto de este tutorial se proporcionan detalles sobre los atributos, pero aquí se muestra el esquema de los elementos que se van a usar:</span><span class="sxs-lookup"><span data-stu-id="b2db4-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="b2db4-115">Teniendo en cuenta la estructura simple de los elementos, puede tener sentido los atributos que hacen que cada elemento sea único.</span><span class="sxs-lookup"><span data-stu-id="b2db4-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="b2db4-116">Los detalles de cada elemento se tratarán en los temas restantes de esta sección.</span><span class="sxs-lookup"><span data-stu-id="b2db4-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="b2db4-117">Para obtener más información sobre los elementos y atributos, vea la [referencia de programación](skin-programming-reference.md)de la máscara.</span><span class="sxs-lookup"><span data-stu-id="b2db4-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2db4-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2db4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2db4-119">**Crear el archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="b2db4-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




