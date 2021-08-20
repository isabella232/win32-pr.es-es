---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18f0e04ed0b2aba3b0637ca8535e2ca5a18110ee29edb397fc250944035f895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115335"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Texto

El elemento del mismo nivel duplicado Name+Role \\ {0} \\ " " provocará ambigüedad entre los elementos.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento tiene los mismos Name y Role/ControlType que otro elemento.

Este problema puede causar confusión porque los lectores de pantalla leerán el mismo texto para todos los elementos con el mismo Nombre y Role/ControlType.

## <a name="possible-causes"></a>Causas posibles

-   El nombre del elemento contiene texto Role/ControlType.
-   El nombre del elemento o el nombre de su elemento primario no se establece o no se establece correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> <dt>

[**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




