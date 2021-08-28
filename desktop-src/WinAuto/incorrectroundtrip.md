---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644745"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Texto

Llame a accNavigate((Haga clic en Snooze para que se le recuerde de nuevo en:), 1, NAVDIR NEXT y, a continuación, accNavigate((Open), 2, NAVDIR PREVIOUS), debe haber devuelto Click Snooze para que se le recuerde de nuevo \_ \_ en:(ChildId=1), pero devolvió Click Snooze para que se le recuerde de nuevo en:

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El [**uso de accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para recorrer el árbol de elementos del destino de comprobación no devuelve el mismo elemento inicial cuando se invierte la dirección del recorrido.

![ejemplo de una implementación de msaa no válida que produjo una navegación de ida y vuelta incorrecta](images/accchecker-invalid-round-trip.png)

Este problema puede causar problemas de navegación para las herramientas automatizadas porque el recorrido de elementos puede ser errático e impredecible.

## <a name="possible-causes"></a>Causas posibles

Una implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




