---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 885a5d930892d6e202764de8e58371f02690edee6715155f34533aaa110d7080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829194"
---
# <a name="elementschildhasdifferentparent"></a>ElementsChildHasDifferentParent

## <a name="text"></a>Texto

El elemento secundario del elemento ( {0} ) tiene un elemento primario diferente( ) que el {1} elemento

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error indica que, cuando se llama a [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en los elementos secundarios del elemento de destino, los elementos secundarios no informan de un elemento primario coherente.

![un ejemplo de los elementos secundarios de un elemento que informa de un elemento primario incoherente](images/accchecker-inconsistent-parent.png)

Este problema puede causar problemas de navegación para las herramientas automatizadas porque los elementos de recorrido pueden ser erráticos e impredecibles.

## <a name="possible-causes"></a>Causas posibles

Una implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




