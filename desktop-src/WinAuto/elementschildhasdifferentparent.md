---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357767"
---
# <a name="elementschildhasdifferentparent"></a>ElementsChildHasDifferentParent

## <a name="text"></a>Texto

El elemento secundario del elemento ( {0} ) tiene distintos elementos primarios ( {1} ) que

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error indica que, cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en los elementos secundarios del elemento de destino, los elementos secundarios no informan de un elemento primario coherente.

![un ejemplo de los elementos secundarios de un elemento que informa de un elemento primario incoherente](images/accchecker-inconsistent-parent.png)

Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.

## <a name="possible-causes"></a>Causas posibles

Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




