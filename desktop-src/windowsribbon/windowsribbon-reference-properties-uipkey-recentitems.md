---
title: UI_PKEY_RecentItems
description: Identifica la propiedad \_ RecentItems de PKEY \_ de la interfaz de usuario.
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437961"
---
# <a name="ui_pkey_recentitems"></a>Elementos \_ recientes de PKEY de la interfaz de \_ usuario

Identifica la propiedad \_ RecentItems de PKEY \_ de la interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Comentarios

[Interfaz de usuario \_ Una aplicación usa PKEY \_ Pinned](windowsribbon-reference-properties-uipkey-pinned.md) para consultar la matriz de elementos de la colección de elementos usados más recientemente (MRU) del [menú de la aplicación](windowsribbon-controls-applicationmenu.md). La información de cada elemento de MRU se encapsula en un [**objeto IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e incluye las tres claves de propiedad siguientes:

-   [Etiqueta \_ PKEY de la interfaz de \_ usuario](windowsribbon-reference-properties-uipkey-label.md)
-   [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [UI \_ PKEY \_ Pinned](windowsribbon-reference-properties-uipkey-pinned.md)

La lista de elementos MRU se pasa a la aplicación host de la cinta de opciones como **SAFEARRAY** de [**punteros IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a las implementaciones respectivas en la aplicación host.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de estado](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 