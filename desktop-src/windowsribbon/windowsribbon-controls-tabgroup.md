---
title: Grupo de pestañas
description: Un grupo de pestañas es un control contextual que se oculta o se muestra en tiempo de ejecución, en función del estado del documento o del área de trabajo. El grupo de pestañas contiene un conjunto de controles de ficha relacionados con el contexto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359265"
---
# <a name="tab-group"></a>Grupo de pestañas

Un grupo de pestañas es un control contextual que se oculta o se muestra en tiempo de ejecución, en función del estado del documento o del área de trabajo. El grupo de pestañas contiene un conjunto de controles de [ficha](windowsribbon-controls-tab.md) relacionados con el contexto.

-   [Detalles](#details)
-   [Propiedades del grupo de pestañas](#tab-group-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

Normalmente, se muestra un grupo de pestañas durante los Estados específicos del documento o del área de trabajo, como cuando un usuario selecciona un tipo de objeto determinado. Por ejemplo, la selección de una imagen contenida en el encabezado de una tabla podría requerir que se muestren varias pestañas contextuales que exponen la funcionalidad de tabla e imagen.

> [!IMPORTANT]
> Un grupo de pestañas no admite los [modos de aplicación](ribbon-applicationmodes.md). Sin embargo, los controles de [ficha](windowsribbon-controls-tab.md) individuales dentro de un grupo de pestañas pueden.

 

En la siguiente captura de pantalla se muestra una [pestaña](windowsribbon-controls-tab.md) contextual de Paint de Windows 7.

![captura de pantalla que muestra un control de pestaña contextual.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Propiedades del grupo de pestañas

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de grupo de pestañas.

Normalmente, una propiedad de grupo de pestañas se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de grupo de pestañas.



| Clave de propiedad                                                                                     | Notas                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [\_Etiqueta PKEY de IU \_](windowsribbon-reference-properties-uipkey-label.md)                           | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado TabGroup**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 