---
title: ControlShouldValue
description: ControlShouldValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ced460fac38552e0b82396e6bbbcf92e90c341e40b289e332a3f188c7e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998745"
---
# <a name="controlshouldhavevalue"></a>ControlShouldValue

## <a name="text"></a>Texto

Un control con el rol de debe tener un valor, pero no se implementa {0} get \_ accValue

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento no proporciona un valor según lo previsto en función del rol MSAA asignado, lo que implica que el elemento no tiene implementado el método [**\_ get accValue.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) Por ejemplo, los siguientes roles de MSAA deben proporcionar un valor.

-   CUADRO \_ COMBINADO DEL SISTEMA DE \_ ROLES
-   ROLE \_ SYSTEM \_ IPADDRESS
-   VÍNCULO \_ DEL SISTEMA DE \_ ROL
-   ROLE \_ SYSTEM \_ OUTLINEITEM
-   BARRA \_ DE PROGRESO DEL SISTEMA DE \_ ROLES
-   CONTROL DESLIZANTE \_ DEL SISTEMA \_ DE ROLES
-   BOTÓN \_ \_ SPINBUTTON DEL SISTEMA DE ROL
-   BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL
-   TEXTO \_ DEL SISTEMA DE \_ ROL

Este problema es un problema para las personas que dependen de un lector de pantalla y un teclado para la navegación, ya que un elemento que tiene un valor intrínseco debe ser capaz de notificar ese valor a un usuario.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un rol MSAA establecido de forma inapropiada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Roles de objeto**](object-roles.md)
</dt> </dl>

 

 




