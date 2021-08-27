---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd040cda80e9dcb19543c8ee5134271693546dfdb8af76053b5a281340080765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122475"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate \_ ReturnedElementWithIncorrectParent

## <a name="text"></a>Texto

Al llamar a accNavigate((Live Search), 0, NAVDIR FIRSTCHILD) que devolvió (x-gadget:///gadget.html) se devolvió el elemento primario incorrecto( NULL ) y no \_ \[ \] (Live Search)

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Cuando se llama [**a get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento secundario devuelto por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (mediante las constantes de navegación NAVDIR FIRSTCHILD o NAVDIR LASTCHILD), el elemento primario devuelto no coincide con el elemento primario especificado en la \_ llamada \_ **accNavigate.**

![ejemplo de una implementación de msaa no válida que devuelve un elemento primario incorrecto.](images/accchecker-invalid-msaa-parent.png)

Este problema puede causar problemas de navegación para las herramientas automatizadas porque los elementos de recorrido pueden ser erráticos e impredecibles.

## <a name="possible-causes"></a>Causas posibles

Una implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




