---
title: TextEdit (patrón de control)
description: Presenta directrices y convenciones para implementar ITextEditProvider, incluida información sobre propiedades y métodos.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control TextEdit
- Automatización de la interfaz de usuario, patrón de control TextEdit
- patrones de control,TextEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567336"
---
# <a name="textedit-control-pattern"></a>TextEdit (patrón de control)

Presenta directrices y convenciones para implementar [**ITextEditProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)incluida información sobre propiedades y métodos. El patrón de control **TextEdit** se usa para el acceso mediante programación a un control que modifica el texto, por ejemplo, un control que realiza la corrección automática o habilita la composición de entrada.

> [!Note]  
> Las notas de implementación de este tema hacen referencia a las API que proceden de Text Services Framework (TSF). Para obtener más información sobre TSF y la referencia de API, [consulte Text Services Framework](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Miembros necesarios para **ITextEditProvider**

Estas propiedades y métodos son necesarios para implementar la [**interfaz ITextEditProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)



| Miembros requeridos                                                              | Tipo de miembro | Notas                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Método      | Devuelve el intervalo de la conversión actual (ninguno si no hay ninguna conversión). Devuelve la composición activa (en TSF, este es el intervalo marcado por **GUID \_ PROP \_ COMPOSING**). Por ejemplo, con el Editor de métodos de entrada japonés (IME) de Microsoft, este sería el texto subrayado completo. |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Método      | Devuelve el intervalo de destino de conversión actual (ninguno si no hay ninguna conversión). En TSF, este es el intervalo de caracteres marcados como **TF \_ ATTR \_ TARGET \_ NOTCONVERTED** o **TF \_ ATTR TARGET \_ \_ CONVERTED** desde la **estructura \_ DISPLAYATTRIBUTE de TF.**                                               |



 

Los **eventos TextEditTextChanged** y **ConversionTargetChanged** deben generarse por microsoft Automatización de la interfaz de usuario que admiten el **patrón TextEdit.**

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   Use la [**función UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) para generar el **evento TextEditTextChanged.**
-   En la tabla siguiente se enumeran los casos en los que debe generar el evento y los parámetros [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) que se usarán.



| TextEditChangeType                                            | Carga del evento                                | Notas                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autocorrección**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Nueva cadena corregida                         | Se genera cuando el control realiza una corrección automática. O bien, siempre que se realiza un reemplazo a través de TSF y el intervalo tiene un valor **\_ GUID PROP \_ TKB \_ ALTERNATES** de **TKB \_ ALTERNATES \_ AUTOCORRECTION \_ APPLIED**.<br/>                                                                                                                                                                   |
| [**Composición**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Cadena actualizada                           | La carga solo debe incluir los caracteres que han cambiado (no enviar toda la cadena de composición). Se genera cada vez que se realiza un reemplazo de composición. En TSF, un reemplazo de composición se define como un reemplazo que tiene establecida la marca **\_ GUID PROP \_ COMPOSING.** Los controles de edición que implementan TSF pueden supervisar estos cambios a través de **la notificación OnEndEdit.**<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | Cadena de composición finalizada (vea Notas) | En TSF, la cadena de conversión que se va a finalizar se define mediante la marca **\_ GUID PROP \_ COMPOSING** que se quita de una composición. Los controles de edición que implementan TSF deben determinar la cadena finalizada de **EndComposition** y generar el evento cuando se llama a **OnEndEdit.**<br/> La cadena de composición finalizada puede estar vacía si se canceló o eliminó la composición.<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   **ConversionTargetChanged se** produce cuando el destino de conversión cambia de un destino a otro.
-   Use la [**función UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) para generar el evento **ConversionTargetChanged** (pase el identificador de evento [**\_ TextEdit \_ ConversionTargetChangedEventId de UIA).**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**)
-   **ConversionTargetChanged** no debe generarse cuando cambia el contenido del destino. Si el cambio de destino se produce simultáneamente con un cambio de composición, el evento de cambio de destino debe generarse después de que ya se hayan producido eventos de composición.
-   En TSF, el destino de conversión se define mediante el valor **TF \_ ATTR \_ TARGET \_ CONVERTED** que se establece desde la **estructura \_ DISPLAYATTRIBUTE de TF.** Los cambios se pueden supervisar mediante **OnEndEdit**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

