---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269146"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Texto

Llame a accNavigate (haga clic en posponer para que se le vuelva a recordar en:), 1, NAVDIR \_ siguiente) y, después, accNavigate ((abierto), 2, NAVDIR \_ anterior), debe haber devuelto hacer clic en posponer para que se le vuelva a recordar en: (ChildId = 1), pero devolvió hacer clic en posponer para volver a tener en cuenta:

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

el uso de [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para recorrer el árbol de elementos del destino de la comprobación no devuelve el mismo elemento inicial cuando se invierte la dirección del recorrido.

![ejemplo de una implementación de MSAA no válida que causó una navegación de ida y vuelta incorrecta](images/accchecker-invalid-round-trip.png)

Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.

## <a name="possible-causes"></a>Causas posibles

Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




