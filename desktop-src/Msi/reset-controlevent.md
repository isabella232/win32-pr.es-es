---
description: Se restablece el cuadro de diálogo. En otras palabras, se llama a todos los controles del cuadro de diálogo para deshacer los cambios de propiedad que han realizado. Este evento restablece todos los valores de propiedad a los que tenían cuando se creó el cuadro de diálogo.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Restablecer ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667666"
---
# <a name="reset-controlevent"></a>Restablecer ControlEvent,

Se restablece el cuadro de diálogo. En otras palabras, se llama a todos los controles del cuadro de diálogo para deshacer los cambios de propiedad que han realizado. Este evento restablece todos los valores de propiedad a los que tenían cuando se creó el cuadro de diálogo.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Hay un caso, que se debe producir en raras ocasiones en la práctica, que no se controla correctamente en este ControlEvent,. Si hay dos o más controles en el mismo cuadro de diálogo vinculados indirectamente a la misma propiedad y al menos uno de ellos empezó a tener alguna otra propiedad, a veces, este valor de propiedad se restablecerá a su segundo valor.

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Se usa un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal para restablecer todos los valores del cuadro de diálogo y cancelar todos los cambios en la página.

 

 



