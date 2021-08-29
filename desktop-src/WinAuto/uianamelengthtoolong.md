---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId identifier AutomationElement.NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec235897680cde3b024a67745b923e989cfc68db3b154be260c9dcd3510ba10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993975"
---
# <a name="uianamelengthtoolong"></a>UiaNameLengthTooLong

## <a name="text"></a>Texto

El nombre del elemento no debe devolver una cadena mayor que {0} el carácter

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El nombre de un elemento contiene demasiados caracteres. Por ejemplo, el [**método IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) usado para recuperar el nombre UIA de un elemento devuelve una cadena mayor que el límite.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no reconocible y no intuitivo.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tienen un nombre o una etiqueta asignados incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




