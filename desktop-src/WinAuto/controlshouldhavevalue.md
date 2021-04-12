---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268938"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Texto

Un control con el rol de {0} debe tener un valor, pero \_ no se implementa Get accValue

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento no proporciona un valor según lo previsto según el rol de MSAA asignado, lo que implica que el elemento no tiene implementado el método [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) . Por ejemplo, los siguientes roles de MSAA deben proporcionar un valor.

-   \_cuadro combinado de sistema de roles \_
-   \_IPAddress del sistema de roles \_
-   \_vínculo del sistema de roles \_
-   \_OUTLINEITEM del sistema de roles \_
-   \_PROGRESSBAR del sistema de roles \_
-   \_control deslizante del sistema de roles \_
-   \_SPINBUTTON del sistema de roles \_
-   \_barra de desplazamiento del sistema de roles \_
-   \_texto del sistema de roles \_

Este problema es un problema para las personas que usan un lector de pantalla y un teclado para la navegación porque un elemento que tiene un valor intrínseco debe ser capaz de notificar ese valor a un usuario.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un rol de MSAA establecido incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Roles de objeto**](object-roles.md)
</dt> </dl>

 

 




