---
description: Este evento está publicado por el control ScrollableText para permitir que el usuario imprima el contenido de ese control.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913262"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent,

Este evento está publicado por el [control ScrollableText](scrollabletext-control.md) para permitir que el usuario imprima el contenido de ese control.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este ControlEvent, está disponible a partir de Windows Installer 5,0.

Un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el [control ScrollableText](scrollabletext-control.md)debe suscribirse a este evento. TheMsiPrint ControlEvent, se debe crear en la [tabla ControlEvent,](controlevent-table.md).

## <a name="published-by"></a>Publicado por

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo que el [control ScrollableText](scrollabletext-control.md) se puede usar para mostrar un cuadro de diálogo modal que permita al usuario imprimir el contenido del control ScrollableText.

 

 



