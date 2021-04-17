---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559165"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate \_ ReturnedElementWithIncorrectParent

## <a name="text"></a>Texto

La llamada a accNavigate ((Live Search), 0, NAVDIR \_ FIRSTCHILD) que devolvió (x-gadget:///gadget.html) devolvió el elemento primario incorrecto ( \[ null \] ) y no (Live Search)

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento secundario devuelto por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (mediante las \_ constantes de navegación NAVDIR FIRSTCHILD o NAVDIR \_ LASTCHILD), el elemento primario devuelto no coincide con el elemento primario especificado en la llamada **accNavigate** .

![ejemplo de una implementación de MSAA no válida que devuelve un elemento primario incorrecto.](images/accchecker-invalid-msaa-parent.png)

Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.

## <a name="possible-causes"></a>Causas posibles

Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




