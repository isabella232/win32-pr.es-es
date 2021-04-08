---
title: UI_PKEY_ItemsSource
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793252"
---
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="0bbdd-103">UI \_ PKEY \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="0bbdd-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="0bbdd-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0bbdd-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="0bbdd-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bbdd-105">Remarks</span></span>

<span data-ttu-id="0bbdd-106">La \_ interfaz \_ de usuario PKEY ItemsSource la usa una aplicación para consultar la colección de elementos de un control de galería, como la barra de herramientas de acceso rápido (Qat).</span><span class="sxs-lookup"><span data-stu-id="0bbdd-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="0bbdd-107">El valor de propiedad es un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="0bbdd-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="0bbdd-108">Cada elemento de este [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) debe implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para exponer las propiedades de solo lectura asociadas al elemento, como la etiqueta o la imagen.</span><span class="sxs-lookup"><span data-stu-id="0bbdd-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="0bbdd-109">Para agregar o eliminar elementos de un control Galería en tiempo de ejecución, use los métodos [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="0bbdd-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="0bbdd-110">En la captura de pantalla siguiente se muestra una colección de elementos en un menú [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="0bbdd-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![captura de pantalla que muestra las categorías en una galería de la cinta.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="0bbdd-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bbdd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bbdd-113">Propiedades de la colección</span><span class="sxs-lookup"><span data-stu-id="0bbdd-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 