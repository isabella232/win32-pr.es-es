---
title: Tabulador (marco de cinta de Windows)
description: Una pestaña contiene grupos de controles relacionados.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359648"
---
# <a name="tab-windows-ribbon-framework"></a>Tabulador (marco de cinta de Windows)

Una pestaña contiene [grupos](windowsribbon-controls-group.md) de controles relacionados.

-   [Detalles](#details)
-   [Propiedades de la ficha](#tab-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

Hay tres tipos de pestaña en el marco de la cinta de opciones.



| Tipo               | Descripción                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pestaña principal**       | Pestañas principales que organizan las funciones predeterminadas de la aplicación.                                                                                                                                                                                                                   |
| **Pestaña contextual** | Pestañas que se muestran durante los Estados específicos del documento o del área de trabajo. Por ejemplo, si un usuario selecciona un tipo de objeto determinado, como una imagen contenida en el encabezado de una tabla, pueden mostrarse varias pestañas contextuales que exponen la funcionalidad de tabla e imagen. |
| **Pestaña modal**      | Pestañas principales que se muestran durante un documento o [modo de aplicación](ribbon-applicationmodes.md)de área de trabajo específico, como la vista previa de impresión.                                                                                                                                        |



 

En la siguiente captura de pantalla se muestra una pestaña básica de Paint de Windows 7.

![captura de pantalla que muestra un control de ficha principal.](images/controls/coretab.png)

## <a name="tab-properties"></a>Propiedades de la ficha

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de pestaña.

Normalmente, una propiedad de ficha se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de pestaña.



| Clave de propiedad                                                                                     | Notas                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_Etiqueta PKEY de IU \_](windowsribbon-reference-properties-uipkey-label.md)                           | Solo se puede actualizar a través de la invalidación. |
| [KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Solo se puede actualizar a través de la invalidación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado de tabulación**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
