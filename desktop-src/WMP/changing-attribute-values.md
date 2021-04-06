---
title: Cambiar valores de atributo
description: Cambiar valores de atributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
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
- atributos, cambiar valores
- cambiar valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075873"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="66ffd-114">Cambiar valores de atributo</span><span class="sxs-lookup"><span data-stu-id="66ffd-114">Changing Attribute Values</span></span>

<span data-ttu-id="66ffd-115">Puede cambiar el valor de un atributo si su página web o aplicación tiene acceso de lectura y escritura a la biblioteca y el atributo se puede leer y escribir.</span><span class="sxs-lookup"><span data-stu-id="66ffd-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="66ffd-116">Puede cambiar un atributo del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="66ffd-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="66ffd-117">Para cambiar los atributos de varios elementos multimedia, puede asignar cada uno de ellos a su vez al *reproductor*. propiedad **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="66ffd-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="66ffd-118">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="66ffd-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="66ffd-119">Para cambiar un atributo, llame al *reproductor*. *currentMedia*. método **setItemInfo** tal como se muestra en el siguiente ejemplo de C#.</span><span class="sxs-lookup"><span data-stu-id="66ffd-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="66ffd-120">Se recomienda llamar a los *medios*. método **isReadOnlyItem** para determinar si se puede cambiar un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="66ffd-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="66ffd-121">Si incrusta el control en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="66ffd-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="66ffd-122">Si utiliza el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios.</span><span class="sxs-lookup"><span data-stu-id="66ffd-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="66ffd-123">En cualquier caso, los cambios están disponibles inmediatamente a través de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="66ffd-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="66ffd-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66ffd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66ffd-125">**Atributos de elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="66ffd-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="66ffd-126">**Acceso a bibliotecas**</span><span class="sxs-lookup"><span data-stu-id="66ffd-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="66ffd-127">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="66ffd-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="66ffd-128">**Leer valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="66ffd-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 




