---
title: Leer valores de atributo
description: Leer valores de atributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, leer valores
- leer valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704755"
---
# <a name="reading-attribute-values"></a><span data-ttu-id="1e81e-114">Leer valores de atributo</span><span class="sxs-lookup"><span data-stu-id="1e81e-114">Reading Attribute Values</span></span>

<span data-ttu-id="1e81e-115">Los atributos que puede encontrar en la biblioteca y en los archivos de Windows Media tienen nombres predefinidos.</span><span class="sxs-lookup"><span data-stu-id="1e81e-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="1e81e-116">Puede escribir código que recupere el valor de un atributo pasando el nombre de ese atributo a un *medio*. **getItemInfo** o *multimedia*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1e81e-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="1e81e-117">También puede escribir código que recupere los valores de todos los atributos de un archivo o un elemento.</span><span class="sxs-lookup"><span data-stu-id="1e81e-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="1e81e-118">En el siguiente ejemplo de C# se recupera el valor del atributo **title** y se muestra en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1e81e-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="1e81e-119">En este ejemplo, el objeto **Player** se definió como AxWMPLib. AxWindowsMediaPlayer Player.</span><span class="sxs-lookup"><span data-stu-id="1e81e-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



<span data-ttu-id="1e81e-120">En la llamada a **getItemInfoByType**, el segundo parámetro es una cadena que especifica el idioma.</span><span class="sxs-lookup"><span data-stu-id="1e81e-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="1e81e-121">Si pasa una cadena vacía como se muestra en este ejemplo, el método recupera el valor en el idioma predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1e81e-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="1e81e-122">Para obtener información sobre el tercer parámetro, vea [atributos con varios valores](attributes-with-multiple-values.md).</span><span class="sxs-lookup"><span data-stu-id="1e81e-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="1e81e-123">En el siguiente ejemplo de C# se recuperan los valores de un atributo determinado en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="1e81e-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="1e81e-124">Devuelve estos valores como una cadena delimitada por signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="1e81e-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="1e81e-125">Tenga en cuenta que para los atributos representados como objetos, como **WM/Letras \_ sincronizadas**, **WM/imagen** y **WM/UserWebURL**, la función devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1e81e-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



<span data-ttu-id="1e81e-126">El tercer argumento que se pasa al método **getItemInfoByType** es el índice de un atributo determinado en un conjunto de atributos con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="1e81e-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="1e81e-127">Puede usar código similar para recuperar los atributos que tienen nombres únicos.</span><span class="sxs-lookup"><span data-stu-id="1e81e-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="1e81e-128">En estos casos, **getAttributeCountByType** devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="1e81e-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="1e81e-129">En el ejemplo mostrado anteriormente, la llamada a **getItemInfoByType** se ejecutaría una sola vez.</span><span class="sxs-lookup"><span data-stu-id="1e81e-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e81e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e81e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e81e-131">**Cambiar valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="1e81e-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="1e81e-132">**Atributos de elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="1e81e-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e81e-133">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="1e81e-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1e81e-134">**Leer valores de atributo de un CD o DVD**</span><span class="sxs-lookup"><span data-stu-id="1e81e-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




