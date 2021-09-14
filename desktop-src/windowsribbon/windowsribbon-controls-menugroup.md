---
title: Grupo de menús
description: El grupo de menús organiza los comandos y controles relacionados dentro de un menú o barra de herramientas.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251732"
---
# <a name="menu-group"></a>Grupo de menús

El grupo de menús organiza los comandos y controles relacionados dentro de un menú o barra de herramientas.

-   [Introducción](#introduction)
-   [Propiedades del grupo de menús](#menu-group-properties)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El control Grupo de menús, que se expone a través del elemento de marcado [**MenuGroup,**](windowsribbon-element-menugroup.md) es un contenedor lógico para grupos de elementos o comandos en controles basados en menús, incluida la [mini](windowsribbon-controls-contextpopup.md) barra de herramientas emergente contextual.

Se puede especificar una etiqueta para un grupo de menús mediante el atributo *LabelTitle* o [**la propiedad Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) de una declaración Command asociada. El valor asignado a *LabelTitle* se representa como un encabezado de categoría.

En el ejemplo siguiente se muestra el marcado Comando para un control [Botón](windowsribbon-controls-splitbutton.md) de división que incluye dos declaraciones de comando de grupo de menús.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



En el ejemplo siguiente se muestra el marcado necesario para un [**elemento SplitButton**](windowsribbon-element-splitbutton.md) con tres declaraciones de elemento [**MenuGroup,**](windowsribbon-element-menugroup.md) dos de las cuales están asociadas a los comandos de grupo de menús del ejemplo anterior. El *atributo Class* del elemento **MenuGroup** se usa para especificar el tamaño de los elementos de menú.


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



En la captura de pantalla siguiente se muestra el menú (con tres controles De grupo de menús) que se genera a partir del marcado en los ejemplos anteriores.

![captura de pantalla de un menú con tres controles de grupo de menús.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>Propiedades del grupo de menús

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Grupo de menús.

Normalmente, una propiedad Grupo de menús se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Grupo de menús.



| Clave de propiedad                                                                                     | Notas                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ui \_ PKEY \_ habilitado](windowsribbon-reference-properties-uipkey-enabled.md)                       | Admite [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [Información sobre \_ claves PKEY \_ de la interfaz de usuario](windowsribbon-reference-properties-uipkey-keytip.md)                         | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md)                           | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado MenuGroup**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 