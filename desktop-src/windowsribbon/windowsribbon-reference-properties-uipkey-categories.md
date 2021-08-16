---
title: UI_PKEY_Categories
description: Identifica la propiedad Ui \_ PKEY \_ Categories.
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4aa812673f289b80b000710dd48a449656368f00d0beb51dcb489e60328e6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086557"
---
# <a name="ui_pkey_categories"></a>Categorías \_ PKEY de la \_ interfaz de usuario

Identifica la propiedad Ui \_ PKEY \_ Categories.

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Comentarios

Las categorías PKEY de la interfaz de usuario las usa una aplicación para consultar las categorías que se usan para agrupar \_ elementos relacionados en un control de \_ galería.

El valor de propiedad es un [**objeto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) donde cada elemento de la colección representa una categoría.

Cada elemento de [**esta IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) debe implementar [**IUISimplePropertySet para**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) exponer las propiedades de solo lectura asociadas al elemento, como la etiqueta o la imagen.

Para agregar o eliminar elementos de un control de galería en tiempo de ejecución, use los distintos métodos de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

En la captura de pantalla siguiente se muestra el uso de dos categorías, Formas de **selección** y **Opciones de selección**, en un menú [**SplitButton.**](windowsribbon-element-splitbutton.md)

![captura de pantalla que muestra dos categorías, formas de selección y opciones de selección, en un control splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la colección](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 