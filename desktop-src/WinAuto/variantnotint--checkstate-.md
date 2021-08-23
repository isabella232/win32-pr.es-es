---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3334a3609e9d64c1bb7109cc6f5bb52a2d09f9f9ac18cc41abf5d761f8e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052173"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Texto

La variante devuelta de {0} debe ser , pero es {1} {2} .

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento informa de un estado MSAA no válido. Por ejemplo, el método [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) usado para recuperar el estado MSAA de un elemento debe devolver un valor entero que represente una de las constantes de estado MSAA, pero en su lugar devuelve otra variante.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque es posible que se notifica al usuario un estado de elemento incorrecto.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tienen un estado MSAA establecido de forma inapropiada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes de estado de objeto**](object-state-constants.md)
</dt> </dl>

 

 




