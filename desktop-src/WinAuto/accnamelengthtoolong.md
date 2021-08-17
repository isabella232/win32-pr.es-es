---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9df4b9001460b9ad96cf5c987a0e8c744ec8df183901494311275052ea4146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327711"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Texto

El nombre del elemento no debe devolver una cadena mayor que {0} el carácter

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El nombre de un elemento contiene demasiados caracteres. Por ejemplo, el [**método get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) utilizado para recuperar el nombre MSAA de un elemento devuelve una cadena mayor que el límite de 32 000 caracteres.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no reconocible y no intuitivo.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tienen un nombre o etiqueta asignados incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




