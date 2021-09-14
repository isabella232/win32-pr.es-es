---
description: El control ScrollableText publica este evento para permitir que el usuario imprima el contenido de ese control.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169761"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent

El control [ScrollableText](scrollabletext-control.md) publica este evento para permitir que el usuario imprima el contenido de ese control.

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este ControlEvent está disponible a partir de Windows Installer 5.0.

Un control [PushButton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control [ScrollableText](scrollabletext-control.md)debe suscribirse a este evento. El control ControlEvent deMsiPrint debe crearse en la [tabla ControlEvent](controlevent-table.md).

## <a name="published-by"></a>Publicado por

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [PushButton](pushbutton-control.md) en el mismo cuadro de diálogo que [el control ScrollableText](scrollabletext-control.md) se puede usar para mostrar un cuadro de diálogo modal que permite al usuario imprimir el contenido del control ScrollableText.

 

 



