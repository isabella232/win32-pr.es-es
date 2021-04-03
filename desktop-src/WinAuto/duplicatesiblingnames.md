---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780047"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Texto

El nombre del mismo nivel y el rol \\ "" duplicados {0} \\ provocarán ambigüedades entre los elementos.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento tiene el mismo nombre y role/ControlType como otro elemento.

Este problema puede causar confusión, ya que los lectores de pantalla leerán el mismo texto para todos los elementos con el mismo nombre y rol/ControlType.

## <a name="possible-causes"></a>Causas posibles

-   El nombre del elemento contiene el texto role/ControlType.
-   El nombre del elemento o el nombre de su elemento primario no está establecido o no se ha establecido correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




