---
description: Al usar varias ventanillas, golpee testingdetermines qué ventanillas se ven afectadas por los datos proporcionados por el usuario tomando la ubicación de la pantalla de un contacto y determinando en qué rectángulo de la ventanilla llega el contacto.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Usar varias ventanillas en DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 627a97a7c9563ca0af9decf79b18340343dda345
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104569797"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Usar varias ventanillas en DirectManipulation

Al usar varias ventanillas, la *prueba de posicionamiento* determina qué ventanillas se ven afectadas por los datos proporcionados por el usuario tomando la ubicación de la pantalla de un contacto y determinando en qué rectángulo de la ventanilla se alcanza el contacto.

Un escenario común en la [manipulación directa](direct-manipulation-portal.md) es colocar una ventanilla dentro de otra, lo que también se conoce como *ventanillas de anidamiento*. Si el contacto alcanza más de una ventanilla, el orden de las llamadas a  [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) por el [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) de la ventana determina la relación de elementos primarios y secundarios de las ventanillas anidadas.

Regla: el elemento secundario debe llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)antes de llamar al elemento primario.

![diagrama que muestra jerarquía de pruebas de posicionamiento](images/dm-art-8.png)

Un contacto aparece en una ventanilla. Primero se debe llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) en la ventanilla naranja (secundaria) y luego en la ventanilla verde (primaria) para establecer la jerarquía correcta.

## <a name="targeting-the-correct-viewport"></a>Establecer como destino la ventanilla correcta

Un contacto puede asociarse a cualquier número de ventanillas y cada contacto se puede asignar a un conjunto diferente de ventanillas.

Cada ventanilla puede configurarse para admitir interacciones específicas, según sea necesario.

Según esta configuración, la [manipulación directa](direct-manipulation-portal.md) identifica qué ventanilla controla la entrada. La ventanilla secundaria de la jerarquía de pruebas de posicionamiento tiene la primera oportunidad de controlar la entrada. Sin embargo, tanto el encadenamiento como la promoción primaria pueden cambiar la ventanilla que controla la entrada.

## <a name="chaining"></a>Encadenamiento

Cuando se alcanza el final del contenido durante una manipulación, la [manipulación directa](direct-manipulation-portal.md) aplica un efecto de límite para indicar que el contenido no puede continuar. Sin embargo, si una ventanilla secundaria está *encadenada* a una ventanilla primaria, se suprime este efecto. En su lugar, la ventanilla antecesora más cercana en la jerarquía de pruebas de posicionamiento que admite la manipulación, controla la entrada. Si se invierte la dirección de la manipulación de manera que el antecesor vuelva al punto en el que se desencadenó el encadenamiento, la manipulación "desencadena" y el control se transfiere de nuevo a la ventanilla secundaria.

![diagrama que muestra la manipulación encadenada](images/dm-art-9.png)

Cuando el usuario gira la ventanilla secundaria hasta el borde del contenido, la manipulación "encadena" a la ventanilla primaria y el usuario comienza a desplazar el contenido primario en su lugar.

> [!Note]  
> La cadena de ejes X e y es independiente entre sí, por lo que si una panorámica diagonal alcanza el límite x antes del límite y, la manipulación mueve el elemento primario en la dirección x mientras continúa moviendo el elemento secundario en la dirección y. Para habilitar o deshabilitar el encadenamiento, llame a la API [**SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) en la ventanilla secundaria.

### <a name="rails"></a>Riel

La especificación de raíles en la configuración de una ventanilla afecta a la manera en que la entrada se encadena desde la ventanilla. En concreto, la entrada no puede encadenar desde una ventanilla secundaria con raíl a su elemento primario en el modo de movimiento panorámico "no entrened" de raíles. Para encadenar la entrada cuando se establecen los raíles, el usuario debe haberse desplazado vertical u horizontalmente y debe estar bloqueado en los raíles.

### <a name="zooming"></a>Acercar o alejar

Si una ventanilla secundaria está anidada dentro de un elemento primario y ambas están configuradas para el zoom, una manipulación del zoom puede encadenarse de un elemento secundario a un elemento primario. Sin embargo, si la manipulación continúa, solo funciona en el elemento primario y no puede "encadenar" en el elemento secundario. Si el usuario encadena un zoom de secundario a primario, la [manipulación directa](direct-manipulation-portal.md) suspende el elemento secundario hasta que todos los contactos asociados a la manipulación se quiten de la pantalla. En este punto, el elemento secundario se libera de la suspensión y el usuario puede desplazar la ventanilla secundaria.

## <a name="gesture-targeting-parent-promotion"></a>Destinatarios de gestos: promoción primaria

La *segmentación de gestos* es el proceso por el que los grupos de [manipulación directa](direct-manipulation-portal.md) se conectan entre sí y determinan qué ventanilla procesa la entrada. La *promoción primaria* hace referencia a los casos donde la entrada se transfiere desde el elemento secundario al elemento primario. Por ejemplo, cuando un usuario coloca dos contactos y se reduce dentro de una ventanilla secundaria configurada solo para el desplazamiento, la entrada se promueve al elemento primario para que se produzca el zoom. La promoción primaria se produce independientemente de si está habilitado el encadenamiento en la ventanilla secundaria.

A diferencia de la encadenamiento, la promoción primaria no se revierte. La ventanilla primaria continúa procesando la entrada de interacción hasta que se levantan todos los contactos (las ventanillas secundarias dejan de procesar la entrada).
