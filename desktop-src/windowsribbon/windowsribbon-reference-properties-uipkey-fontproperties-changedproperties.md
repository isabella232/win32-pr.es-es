---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ChangedProperties.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421166"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a><span data-ttu-id="870fe-103">UI \_ PKEY \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="870fe-103">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>

<span data-ttu-id="870fe-104">Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ChangedProperties.</span><span class="sxs-lookup"><span data-stu-id="870fe-104">Identifies the UI\_PKEY\_FontProperties\_ChangedProperties property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a><span data-ttu-id="870fe-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="870fe-105">Remarks</span></span>

<span data-ttu-id="870fe-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties \_ ChangedProperties para consultar solo las propiedades cambiadas de la [interfaz de usuario \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span><span class="sxs-lookup"><span data-stu-id="870fe-106">UI\_PKEY\_FontProperties\_ChangedProperties is used by an application to query only changed properties from [UI\_PKEY\_FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span></span>

<span data-ttu-id="870fe-107">Al llamar al método [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) en este objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , se devuelve [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="870fe-107">Calling the [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method on this [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object returns an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

<span data-ttu-id="870fe-108">UI \_ PKEY \_ FontProperties \_ ChangedProperties se pasa como el último parámetro de la llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) a la aplicación host de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="870fe-108">UI\_PKEY\_FontProperties\_ChangedProperties is passed as the last parameter of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) call to the Ribbon host application.</span></span>

<span data-ttu-id="870fe-109">Esta clave de propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="870fe-109">This property key is read-only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="870fe-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="870fe-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="870fe-111">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="870fe-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="870fe-112">**IUISimplePropertySet**</span><span class="sxs-lookup"><span data-stu-id="870fe-112">**IUISimplePropertySet**</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[<span data-ttu-id="870fe-113">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="870fe-113">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 