---
description: Cuando se crea un dispositivo, la adquisición de imágenes de Windows (WIA) crea un árbol jerárquico de elementos WIA que representan el dispositivo y las carpetas e imágenes asociadas a ese dispositivo.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Enumerar elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c216e658b7105f6b3d88d01bd55a3200af7e45c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276859"
---
# <a name="enumerating-items"></a><span data-ttu-id="53e5c-103">Enumerar elementos</span><span class="sxs-lookup"><span data-stu-id="53e5c-103">Enumerating Items</span></span>

<span data-ttu-id="53e5c-104">Cuando se crea un dispositivo, la adquisición de imágenes de Windows (WIA) crea un árbol jerárquico de elementos WIA que representan el dispositivo y las carpetas e imágenes asociadas a ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53e5c-104">When a device is created, Windows Image Acquisition (WIA) creates a hierarchical tree of WIA items that represent the device and the folders and images associated with that device.</span></span> <span data-ttu-id="53e5c-105">Use el método del elemento raíz (el elemento en la raíz del árbol que representa el dispositivo) [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (o [**IWiaItem2:: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) para crear un objeto de enumerador y obtener un puntero a su interfaz [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (o [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)), que se usa para navegar por el árbol de elementos y obtener acceso a las imágenes o a los bancos de análisis asociados con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53e5c-105">Use the root item's (the item at the root of the tree that represents the device) [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method to create an enumerator object and obtain a pointer to its [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (or [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) interface, which is used to navigate the item tree and gain access to the images or scanning beds associated with the device.</span></span>

<span data-ttu-id="53e5c-106">En el ejemplo siguiente se muestra una función que enumera de forma recursiva todos los elementos de un árbol, empezando por un elemento raíz que se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="53e5c-106">The following example shows a function that recursively enumerates all of the items of a tree, beginning with a root item that is passed to the function.</span></span>


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



<span data-ttu-id="53e5c-107">La función toma el parámetro **pWiaItem**, un puntero a la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (o [**IWiaItem2**](-wia-iwiaitem2.md)) del elemento raíz del árbol de elementos que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="53e5c-107">The function takes the parameter **pWiaItem**, a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (or [**IWiaItem2**](-wia-iwiaitem2.md)) interface of the root item of the item tree to enumerate.</span></span>

<span data-ttu-id="53e5c-108">En primer lugar, la función comprueba si el elemento es una carpeta o si tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="53e5c-108">First, the function checks to see whether the item is a folder or if it has attachments.</span></span> <span data-ttu-id="53e5c-109">Si es así, llama al método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (o [**IWiaItem2:: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) de **pWiaItem** para crear un objeto de enumerador para el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="53e5c-109">If it does, it then calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method of **pWiaItem** to create an enumerator object for the item tree.</span></span> <span data-ttu-id="53e5c-110">Si esta llamada se realiza correctamente y el enumerador es válido, la función recorre en iteración los elementos secundarios y, de forma recursiva, se llama a sí mismo en cada elemento, tratando cada uno como un posible elemento raíz para el siguiente nivel de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="53e5c-110">If this call succeeds, and the enumerator is valid, the function iterates through the child items, and recursively calls itself on each item, treating each as a potential root item for the next level of child items.</span></span>

<span data-ttu-id="53e5c-111">De esta manera, la función enumera todas las ramas del árbol de elementos debajo del elemento raíz pasado a **EnumerateItems**.</span><span class="sxs-lookup"><span data-stu-id="53e5c-111">In this manner, the function enumerates all branches of the item tree below the root item passed to **EnumerateItems**.</span></span>

 

 



