---
title: Cambiar la posición actual
description: Cambiar la posición actual
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420724"
---
# <a name="changing-the-current-position"></a>Cambiar la posición actual

Para cambiar la posición actual en un elemento de dispositivo, use el mensaje de comando de [**\_ búsqueda de MCI**](mci-seek.md) junto con la estructura de MCI \_ to Flag y [**MCI \_ Seek \_ parms**](mci-seek-parms.md) . Si usa el miembro **dwTo** para especificar una posición de búsqueda con MCI \_ Seek, debe consultar el formato de hora y establecerlo, si es necesario.

Además de especificar una posición con el miembro **dwTo** , puede especificar las marcas de MCI \_ Seek \_ to \_ Start o MCI \_ Seek \_ to \_ end para el parámetro *dwParam1* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para buscar las posiciones inicial y final del elemento de dispositivo. Si usa una de estas marcas, no especifique el MCI \_ que desea marcar.

 

 