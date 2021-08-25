---
title: Botón Ayuda
description: El botón Ayuda es un control en el que el usuario puede hacer clic para mostrar el sistema de ayuda de la aplicación.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 295b3c7feae2aecada128dadbccd093f654c6a6660a68f4790975aee060aaf61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933394"
---
# <a name="help-button"></a>Botón Ayuda

El botón Ayuda es un control en el que el usuario puede hacer clic para mostrar el sistema de ayuda de la aplicación.

-   [Detalles](#details)
-   [Propiedades del botón Ayuda](#help-button-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la siguiente captura de pantalla se muestra el botón Ayuda de la cinta de opciones.

![captura de pantalla que muestra el botón de ayuda.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Propiedades del botón Ayuda

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Botón de ayuda.

Normalmente, una propiedad Botón de ayuda se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El evento de invalidación se controla y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación ha consultado un valor de propiedad actualizado, hasta que el marco requiere la propiedad . Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Botón de ayuda.



| Clave de propiedad                                                                                     | Notas                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Información sobre \_ claves PKEY \_ de la interfaz de usuario](windowsribbon-reference-properties-uipkey-keytip.md)                         | Solo se puede actualizar a través de la invalidación. |
| [Etiqueta \_ PKEY de la interfaz de \_ usuario](windowsribbon-reference-properties-uipkey-label.md)                           | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Solo se puede actualizar a través de la invalidación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento HelpButton**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 