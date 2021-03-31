---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903321"
---
# <a name="uianameshouldnotcontaincontroltype"></a>UiaNameShouldNotContainControlType

## <a name="text"></a>Texto

El nombre del elemento ( {0} ) no debe contener el texto de ControlType ( {1} )

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

El nombre de un elemento incorpora su tipo de control UIA. Por ejemplo, esta advertencia puede producirse si la propiedad de nombre de UIA para un elemento con el tipo de control Button está establecida en "My Button".

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque el tipo de control se leerá dos veces, o puede que no sea pronunciable o no intuitivo para los usuarios.

## <a name="possible-causes"></a>Causas posibles

-   El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.
-   El elemento o su elemento primario tiene un nombre predeterminado que no se ha revisado en un nombre descriptivo. Por ejemplo, button1.
-   Un desarrollador no es consciente de que los lectores de pantalla leen los nombres y los tipos de control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




