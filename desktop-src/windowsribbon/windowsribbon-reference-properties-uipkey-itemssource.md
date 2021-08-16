---
title: UI_PKEY_ItemsSource
description: Identifica la propiedad \_ PKEY ItemsSource de la \_ interfaz de usuario.
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201580"
---
# <a name="ui_pkey_itemssource"></a>UI \_ PKEY \_ ItemsSource

Identifica la propiedad \_ PKEY ItemsSource de la \_ interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Comentarios

La interfaz de usuario PKEY ItemsSource la usa una aplicación para consultar la colección de elementos de un control de galería, como la barra de herramientas de acceso rápido \_ \_ (QAT).

El valor de propiedad es un [**objeto IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Cada elemento de [**esta IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) debe implementar [**IUISimplePropertySet para**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) exponer las propiedades de solo lectura asociadas al elemento, como la etiqueta o la imagen.

Para agregar o eliminar elementos de un control de galería en tiempo de ejecución, use los [**métodos IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

En la siguiente captura de pantalla se muestra una colección de elementos en un [**menú SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

![captura de pantalla que muestra categorías en una galería de cinta de opciones.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la colección](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 