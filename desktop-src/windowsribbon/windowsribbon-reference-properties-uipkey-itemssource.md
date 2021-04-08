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
# <a name="ui_pkey_itemssource"></a>UI \_ PKEY \_ ItemsSource

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Observaciones

La \_ interfaz \_ de usuario PKEY ItemsSource la usa una aplicación para consultar la colección de elementos de un control de galería, como la barra de herramientas de acceso rápido (Qat).

El valor de propiedad es un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Cada elemento de este [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) debe implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para exponer las propiedades de solo lectura asociadas al elemento, como la etiqueta o la imagen.

Para agregar o eliminar elementos de un control Galería en tiempo de ejecución, use los métodos [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

En la captura de pantalla siguiente se muestra una colección de elementos en un menú [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

![captura de pantalla que muestra las categorías en una galería de la cinta.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la colección](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 