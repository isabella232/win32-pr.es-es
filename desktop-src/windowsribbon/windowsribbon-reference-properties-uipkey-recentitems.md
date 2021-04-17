---
title: UI_PKEY_RecentItems
description: Identifica la propiedad RecentItems de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714401"
---
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="a4e60-103">UI \_ PKEY \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="a4e60-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="a4e60-104">Identifica la propiedad RecentItems de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a4e60-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="a4e60-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4e60-105">Remarks</span></span>

<span data-ttu-id="a4e60-106">[Interfaz de usuario \_ Una aplicación usa PKEY \_ anclado](windowsribbon-reference-properties-uipkey-pinned.md) para consultar la matriz de elementos de la colección de elementos usados más recientemente (MRU) del menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="a4e60-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="a4e60-107">La información de cada elemento MRU se encapsula en un objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e incluye las tres claves de propiedad siguientes:</span><span class="sxs-lookup"><span data-stu-id="a4e60-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="a4e60-108">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="a4e60-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="a4e60-109">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="a4e60-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="a4e60-110">Interfaz de usuario \_ PKEY \_ anclada</span><span class="sxs-lookup"><span data-stu-id="a4e60-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="a4e60-111">La lista de elementos MRU se pasa a la aplicación host de cinta como una **matriz SafeArray** de punteros [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a implementaciones respectivas en la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="a4e60-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4e60-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4e60-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e60-113">Propiedades de estado</span><span class="sxs-lookup"><span data-stu-id="a4e60-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 