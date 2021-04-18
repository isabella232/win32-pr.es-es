---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704788"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Texto

El nombre del elemento no debe devolver una cadena más larga que el {0} carácter

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El nombre de un elemento contiene demasiados caracteres. Por ejemplo, el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) que se usa para recuperar el nombre de MSAA de un elemento devuelve una cadena mayor que el límite de 32000 caracteres.

Este problema causa problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no descriptivo y no intuitivo.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




