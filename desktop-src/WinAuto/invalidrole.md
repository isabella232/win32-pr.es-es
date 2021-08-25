---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acecf91e90f93ccb1d220e9b2d91cbaa012b8d436b18a910daa73bf6ca3f1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860005"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Texto

El valor int devuelto por get \_ accRole no es una constante de rol válida, es decir, ROLE \_ SYSTEM\_\*

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento informa de un rol MSAA no válido. Por ejemplo, el [**método get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) devuelve un valor entero que no se asigna a una constante de rol de objeto válida (como ROLE \_ SYSTEM \_ LISTITEM).

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque los elementos pueden identificarse incorrectamente para el usuario.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tienen un rol MSAA establecido de forma inapropiada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Roles de objeto**](object-roles.md)
</dt> </dl>

 

 




