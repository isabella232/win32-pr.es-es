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
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ PKEY \_ FontProperties \_ ChangedProperties

Identifica la propiedad PKEY de la interfaz de usuario \_ \_ FontProperties \_ ChangedProperties.

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY FontProperties \_ ChangedProperties para consultar solo las propiedades cambiadas de la [interfaz de usuario \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

Al llamar al método [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) en este objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , se devuelve [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).

UI \_ PKEY \_ FontProperties \_ ChangedProperties se pasa como el último parámetro de la llamada [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) a la aplicación host de la cinta de opciones.

Esta clave de propiedad es de solo lectura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 