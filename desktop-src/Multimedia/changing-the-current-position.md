---
title: Cambiar la posición actual
description: Cambiar la posición actual
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14f062fc93a89f54fb89a30b6ac3e53c8d6240cfc28b661a25da48a0b1b2fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941293"
---
# <a name="changing-the-current-position"></a>Cambiar la posición actual

Para cambiar la posición actual en un elemento de dispositivo, use el mensaje de comando [**\_ MCI SEEK**](mci-seek.md) junto con la marca TO de MCI y la estructura \_ [**MCI SEEK \_ \_ PARMS.**](mci-seek-parms.md) Si usa el miembro **dwTo** para especificar una posición de búsqueda con MCI SEEK, debe consultar el formato de hora y \_ establecerlo, si es necesario.

Además de especificar una posición con el miembro **dwTo,** puede especificar las marcas MCI SEEK TO START o MCI SEEK TO END para el parámetro dwParam1 de la función \_ \_ \_ \_ \_ \_ [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))  para buscar las posiciones inicial y final del elemento device. Si usa una de estas marcas, no especifique la marca MCI \_ TO.

 

 