---
description: El control SelectionTree usa el evento SelectionBrowse para generar un cuadro de diálogo de exploración que permita modificar la ruta de acceso del elemento resaltado.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361644"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionBrowse para generar un cuadro de diálogo de **exploración** que permita modificar la ruta de acceso del elemento resaltado.

Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Los controles que publican un evento SelectionBrowse se deshabilitan si se ha seleccionado una característica que ya está instalada, no es configurable o no se ha seleccionado para la instalación local. Para ser configurables, la característica debe tener una [propiedad pública](public-properties.md) especificada en el \_ campo directorio de la [tabla de características](feature-table.md).

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nombre del cuadro de diálogo que se va a generar.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el SelectionTree usa este evento para desencadenar el cuadro de diálogo **examinar** .

 

 



