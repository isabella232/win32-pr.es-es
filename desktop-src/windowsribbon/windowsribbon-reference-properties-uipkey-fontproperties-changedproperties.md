---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifica la propiedad \_ FontProperties ChangedProperties de la interfaz de usuario \_ PKEY. \_
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36262a9acf217e448956f108b68cb0716b5b5080c71f6a2a8e305c9e59478c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028663"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ PKEY \_ FontProperties \_ ChangedProperties

Identifica la propiedad \_ FontProperties ChangedProperties de la interfaz de usuario \_ PKEY. \_

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Comentarios

La \_ interfaz de usuario PKEY FontProperties ChangedProperties se usa en una aplicación para consultar solo las propiedades modificadas de la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

Al llamar [**al método IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) en este objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) se devuelve [un objeto IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).

La interfaz de usuario PKEY FontProperties ChangedProperties se pasa como el último parámetro de la \_ \_ llamada \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) a la aplicación host de la cinta de opciones.

Esta clave de propiedad es de solo lectura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 