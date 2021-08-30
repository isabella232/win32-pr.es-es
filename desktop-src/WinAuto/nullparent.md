---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f265f66eb4d0b0985d9f3979fc7ff4b9bb1812df1617cdaa4f6f50d7b357e067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998155"
---
# <a name="nullparent"></a>NullParent

## <a name="text"></a>Texto

El elemento primario elements es NULL

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Se devuelve NULL cuando [**se llama a get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento . El **método get \_ accParent** solo debe devolver NULL cuando se llama en el elemento raíz del destino de comprobación.

Este problema puede causar problemas de navegación para las herramientas automatizadas porque el recorrido de elementos puede ser errático e impredecible.

## <a name="possible-causes"></a>Causas posibles

Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




