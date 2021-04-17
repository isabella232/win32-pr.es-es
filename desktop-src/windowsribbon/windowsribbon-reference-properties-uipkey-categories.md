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
# <a name="ui_pkey_categories"></a>\_Categorías de PKEY de IU \_

Identifica la propiedad de las categorías PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Observaciones

Las categorías de PKEY de interfaz de usuario \_ \_ se usan en una aplicación para consultar las categorías que se usan para agrupar elementos relacionados en un control de galería.

El valor de propiedad es un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) donde cada elemento de la colección representa una categoría.

Cada elemento de este [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) debe implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para exponer las propiedades de solo lectura asociadas al elemento, como la etiqueta o la imagen.

Para agregar o eliminar elementos de un control Galería en tiempo de ejecución, use los distintos métodos de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

En la captura de pantalla siguiente se muestra el uso de dos categorías, las **formas de selección** y **las opciones de selección**, en un menú de [**splitButton**](windowsribbon-element-splitbutton.md) .

![captura de pantalla que muestra dos categorías, las formas de selección y las opciones de selección, en un control splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la colección](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 