---
description: SpawnDialog ControlEvent, notifica al instalador que cree un elemento secundario de un cuadro de diálogo modal mientras mantiene el cuadro de diálogo presente en ejecución.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677301"
---
# <a name="spawndialog-controlevent"></a>SpawnDialog ControlEvent,

SpawnDialog ControlEvent, notifica al instalador que cree un elemento secundario de un cuadro de diálogo modal mientras mantiene el cuadro de diálogo presente en ejecución.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Cadena que es el nombre del nuevo cuadro de diálogo.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para crear un cuadro de diálogo secundario, como "¿está seguro de que desea cancelar?" .

 

 



