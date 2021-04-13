---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357158"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole)

## <a name="text"></a>Texto

La variante devuelta de {0} debe ser una {1} pero es {2} .

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento está informando de un rol de MSAA no válido. Por ejemplo, el método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que se usa para recuperar el rol de MSAA de un elemento debe devolver un valor entero que represente una de las constantes de rol de MSAA, pero que devuelve otra variante en su lugar.

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se pueden identificar incorrectamente al usuario.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un rol de MSAA establecido incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Roles de objeto**](object-roles.md)
</dt> </dl>

 

 




