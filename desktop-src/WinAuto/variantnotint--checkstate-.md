---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268786"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Texto

La variante devuelta de {0} debe ser una {1} pero es {2} .

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento está informando de un estado de MSAA no válido. Por ejemplo, el método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) que se usa para recuperar el estado de MSAA de un elemento debe devolver un valor entero que represente una de las constantes de estado de MSAA, pero que devuelve otra variante en su lugar.

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque es posible que se notifique al usuario un estado incorrecto del elemento.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un estado de MSAA establecido incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes de estado de objeto**](object-state-constants.md)
</dt> </dl>

 

 




