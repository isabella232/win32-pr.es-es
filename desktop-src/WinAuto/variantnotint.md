---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b5d06c42668e600b15019277ac7bacb3a07b2058e083b5de4964d1d6c46052
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098025"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole)

## <a name="text"></a>Texto

La variante devuelta de {0} debe ser , pero es {1} {2} .

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento informa de un rol MSAA no válido. Por ejemplo, el método [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) usado para recuperar el rol MSAA de un elemento debe devolver un valor entero que represente una de las constantes de rol de MSAA, pero devuelve otra variante en su lugar.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque los elementos pueden identificarse incorrectamente para el usuario.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un rol MSAA establecido de forma inapropiada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Roles de objeto**](object-roles.md)
</dt> </dl>

 

 




