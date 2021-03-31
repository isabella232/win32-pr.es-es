---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId identificador AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419045"
---
# <a name="uianamelengthtoolong"></a>UiaNameLengthTooLong

## <a name="text"></a>Texto

El nombre del elemento no debe devolver una cadena más larga que el {0} carácter

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El nombre de un elemento contiene demasiados caracteres. Por ejemplo, el método [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) que se usa para recuperar el nombre de UIA de un elemento devuelve una cadena mayor que el límite.

Este problema causa problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no descriptivo y no intuitivo.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




