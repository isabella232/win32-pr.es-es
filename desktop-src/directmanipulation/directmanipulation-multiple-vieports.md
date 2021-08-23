---
description: Cuando se usan varias ventanillas, las pruebas de aciertos determinan qué ventanillas se ven afectadas por la entrada del usuario tomando la ubicación de pantalla de un contacto y determinando qué rectángulo de ventanilla alcanza el contacto.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Uso de varias ventanillas en DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: e422d99d8a71fbf24af5fc60641da7ac808b54215c56e5d81b8c222226ef8452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787535"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Uso de varias ventanillas en DirectManipulation

Cuando se usan varias ventanillas, las pruebas de aciertos determinan qué ventanillas se ven afectadas por la entrada del usuario tomando la ubicación de pantalla de un contacto y determinando qué rectángulo de ventanilla alcanza el contacto.

Un escenario común en [la manipulación directa](direct-manipulation-portal.md) es colocar una ventanilla dentro de otra, también conocida como *anidamiento de ventanillas*. Si el contacto alcanza más de una ventanilla, el orden de  [**llamadas SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) por parte del [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) de la ventana determina la relación de elementos primarios y secundarios de las ventanillas anidadas.

Regla: el elemento secundario debe llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)antes de llamar al elemento primario.

![diagrama que muestra la jerarquía de las pruebas de impacto](images/dm-art-8.png)

Un contacto aparece en una ventanilla. [**Primero se debe**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) llamar a SetContact en la ventanilla naranja (secundaria) y, después, en la ventanilla verde (primaria) para establecer la jerarquía correcta.

## <a name="targeting-the-correct-viewport"></a>Destino de la ventanilla correcta

Un contacto se puede asociar a cualquier número de ventanillas y cada contacto se puede asignar a un conjunto diferente de ventanillas.

Cada ventanilla se puede configurar para admitir interacciones específicas, según sea necesario.

En función de esta configuración, [la manipulación directa](direct-manipulation-portal.md) identifica qué ventanilla controla la entrada. La ventanilla más secundaria de la jerarquía de pruebas de acceso tiene la primera oportunidad de controlar la entrada. Sin embargo, tanto el encadenamiento como la promoción primaria pueden cambiar la ventanilla que controla la entrada.

## <a name="chaining"></a>Encadenamiento

Cuando se alcanza el final del contenido durante una manipulación, [la](direct-manipulation-portal.md) manipulación directa aplica un efecto de límite para indicar que el contenido no puede ir más allá. Sin embargo, si una ventanilla secundaria está *encadenada* a una ventanilla primaria, este efecto se suprime. En su lugar, la ventanilla antecesor más cercana en la jerarquía de pruebas de impacto que admite la manipulación controla la entrada. Si la dirección de la manipulación se invierte de forma que el antecesor vuelve al punto donde se desencadenó el encadenamiento, la manipulación "desencadena" y el control se transfiere de nuevo a la ventanilla secundaria.

![diagrama que muestra la manipulación encadenada](images/dm-art-9.png)

Cuando el usuario hace un desplazamiento panorámico de la ventanilla secundaria hasta el borde del contenido, la manipulación se "encadena" a la ventanilla primaria y el usuario comienza a desplazar el contenido primario en su lugar.

> [!Note]  
> Los ejes X e Y se encadenan de forma independiente entre sí, por lo que si una panorámica diagonal alcanza el límite x antes del límite y, la manipulación mueve el elemento primario en la dirección x mientras se sigue desplazando el elemento secundario en la dirección y. Para habilitar o deshabilitar el encadenamiento, llame a la API [**SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) en la ventanilla secundaria.

### <a name="rails"></a>Carriles

La especificación de raíles en la configuración de una ventanilla afecta a la forma en que la entrada se encadena desde la ventanilla. En concreto, la entrada no puede encadenar desde una ventanilla secundaria con raíl a su elemento primario en el modo de desplazamiento panorámico "sin descarrilar" de los raíles. Para encadenar la entrada cuando se establecen raíles, el usuario debe haber hecho movimientos horizontales vertical u horizontalmente y estar bloqueado en los raíles.

### <a name="zooming"></a>Acercar o alejar

Si una ventanilla secundaria está anidada dentro de un elemento primario y ambas están configuradas para el zoom, una manipulación de zoom se puede encadenar de elemento secundario a primario. Sin embargo, si la manipulación continúa, solo funciona en el elemento primario y no puede "desenlace" con el elemento secundario. Si el usuario encadena un zoom de elemento secundario a primario, [la](direct-manipulation-portal.md) manipulación directa suspende el elemento secundario hasta que todos los contactos asociados a la manipulación se quiten de la pantalla. En este momento, el elemento secundario se libera de la suspensión y el usuario puede desplazarse por la ventanilla secundaria.

## <a name="gesture-targeting-parent-promotion"></a>Destino de gestos: promoción primaria

*La selección de destino de gestos* es el proceso por el que [la](direct-manipulation-portal.md) manipulación directa agrupa los contactos y determina qué ventanilla procesa la entrada. *La promoción primaria* hace referencia a los casos en los que la entrada se transfiere del elemento secundario al primario. Por ejemplo, cuando un usuario coloca dos contactos y se reduce dentro de una ventanilla secundaria configurada solo para el desplazamiento, la entrada se promueve al elemento primario para que se produzca el zoom. La promoción primaria se produce independientemente de si el encadenamiento está habilitado en la ventanilla secundaria.

A diferencia del encadenamiento, la promoción primaria no se invierte. La ventanilla primaria continúa procesando la entrada de interacción hasta que se elevan todos los contactos (las ventanillas secundarias dejan de procesar la entrada).
