---
title: Patrón de control TextEdit
description: Presenta directrices y convenciones para implementar ITextEditProvider, incluida información sobre propiedades y métodos.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control TextEdit
- Automatización de la interfaz de usuario, patrón de control TextEdit
- patrones de control, TextEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359378"
---
# <a name="textedit-control-pattern"></a>Patrón de control TextEdit

Presenta directrices y convenciones para implementar [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider), incluida información sobre propiedades y métodos. El patrón de control **TextEdit** se usa para el acceso mediante programación a un control que modifica texto, por ejemplo, un control que realiza la corrección automática o habilita la composición de entradas.

> [!Note]  
> Las notas de implementación de este tema hacen referencia a las API que proceden de Text Services Framework (TSF). Para obtener más información sobre TSF y la referencia de API, vea [Text Services Framework](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Miembros requeridos para **ITextEditProvider**

Estas propiedades y métodos son necesarios para implementar la interfaz [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) .



| Miembros requeridos                                                              | Tipo de miembro | Notas                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Método      | Devuelve el intervalo de la conversión actual (ninguno si no hay ninguna conversión). Devuelve la composición activa (en TSF, este es el intervalo marcado por el **GUID \_ prop \_ componiendo**). Por ejemplo, con el editor de métodos de entrada (IME) japonés de Microsoft, este sería el texto subrayado completo. |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Método      | Devuelve el intervalo de destino de la conversión actual (ninguno si no hay conversión). En TSF, este es el intervalo de caracteres marcados como destino de **TF \_ ATTR \_ \_ NOTCONVERTED** o **TF \_ ATTR \_ target \_ convertido** a partir de la estructura **TF \_ DISPLAYATTRIBUTE** .                                               |



 

Los elementos de automatización de la interfaz de usuario de Microsoft que admiten el patrón **TextEdit** deben generar los eventos **TextEditTextChanged** y **ConversionTargetChanged** .

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   Utilice la función [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) para generar el evento **TextEditTextChanged** .
-   En la tabla siguiente se enumeran los casos en los que se debe generar el evento y los parámetros [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) que se van a usar.



| TextEditChangeType                                            | Carga del evento                                | Notas                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autocorrección**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Nueva cadena corregida                         | Se genera cuando el control realiza una corrección automática. O cada vez que se realiza un reemplazo a través de TSF y el intervalo tiene un **GUID \_ prop \_ TKB valor \_ alternativo** de **TKB \_ alternativos se \_ \_ aplica la Autocorrección**.<br/>                                                                                                                                                                   |
| [**Composición**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | La cadena actualizada                           | La carga útil solo debe incluir los caracteres que han cambiado (no enviar toda la cadena de composición). Se genera cuando se realiza un reemplazo de composición. En TSF, un reemplazo de composición se define como un reemplazo que tiene establecida la marca de **\_ \_ composición de prop de GUID** . Los controles de edición que implementan TSF pueden supervisar estos cambios a través de la notificación **OnEndEdit** .<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | Cadena de composición finalizada (vea las notas) | En TSF, la cadena de conversión que se va a finalizar se define mediante la marca de composición del **GUID \_ \_** que se va a quitar de una composición. Los controles de edición que implementan TSF deben determinar la cadena finalizada desde **EndComposition** y generar el evento cuando se llama a **OnEndEdit** .<br/> La cadena de composición finalizada puede estar vacía si la composición se canceló o se eliminó.<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   **ConversionTargetChanged** se produce cuando el destino de la conversión cambia de un destino a otro.
-   Use la función [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) para generar el evento **ConversionTargetChanged** (pase el identificador de eventos [**\_ \_ ConversionTargetChangedEventId de UIA TextEdit**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) ).
-   No se debe generar **ConversionTargetChanged** cuando cambia el contenido del destino. Si el cambio de destino se produce de forma simultánea con un cambio de composición, el evento de cambio de destino debe generarse una vez que ya se hayan producido eventos de composición.
-   En TSF, el destino de la conversión se define mediante el valor **TF \_ ATTR \_ target \_ convertido** que se establece a partir de la estructura **TF \_ DISPLAYATTRIBUTE** . Los cambios pueden supervisarse mediante **OnEndEdit**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

