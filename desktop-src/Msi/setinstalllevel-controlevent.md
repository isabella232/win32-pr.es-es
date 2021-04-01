---
description: El evento SetInstallLevel cambia el nivel de instalación al valor especificado por el argumento.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275665"
---
# <a name="setinstalllevel-controlevent"></a>SetInstallLevel ControlEvent,

El evento SetInstallLevel cambia el nivel de instalación al valor especificado por el argumento.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Un entero que es el nuevo valor del nivel de instalación.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para cambiar el nivel de instalación.

 

 



