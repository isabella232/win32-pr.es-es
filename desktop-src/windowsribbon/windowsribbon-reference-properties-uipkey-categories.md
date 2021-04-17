---
title: UI_PKEY_Categories
description: Identifica la propiedad de las categorías PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704983"
---
# <a name="ui_pkey_categories"></a><span data-ttu-id="88f07-103">\_Categorías de PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="88f07-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="88f07-104">Identifica la propiedad de las categorías PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="88f07-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="88f07-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88f07-105">Remarks</span></span>

<span data-ttu-id="88f07-106">Las categorías de PKEY de interfaz de usuario \_ \_ se usan en una aplicación para consultar las categorías que se usan para agrupar elementos relacionados en un control de galería.</span><span class="sxs-lookup"><span data-stu-id="88f07-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="88f07-107">El valor de propiedad es un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) donde cada elemento de la colección representa una categoría.</span><span class="sxs-lookup"><span data-stu-id="88f07-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="88f07-108">Cada elemento de este [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) debe implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para exponer las propiedades de solo lectura asociadas al elemento, como la etiqueta o la imagen.</span><span class="sxs-lookup"><span data-stu-id="88f07-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="88f07-109">Para agregar o eliminar elementos de un control Galería en tiempo de ejecución, use los distintos métodos de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span><span class="sxs-lookup"><span data-stu-id="88f07-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="88f07-110">En la captura de pantalla siguiente se muestra el uso de dos categorías, las **formas de selección** y **las opciones de selección**, en un menú de [**splitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="88f07-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![captura de pantalla que muestra dos categorías, las formas de selección y las opciones de selección, en un control splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="88f07-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88f07-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f07-113">Propiedades de la colección</span><span class="sxs-lookup"><span data-stu-id="88f07-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="88f07-114">UI \_ PKEY \_ CategoryID</span><span class="sxs-lookup"><span data-stu-id="88f07-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 