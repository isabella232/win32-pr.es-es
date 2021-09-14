---
title: Cambiar la posición actual
description: Cambiar la posición actual
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266039"
---
# <a name="changing-the-current-position"></a>Cambiar la posición actual

Para cambiar la posición actual en un elemento de dispositivo, use el mensaje de comando [**\_ MCI SEEK**](mci-seek.md) junto con la marca MCI TO y la estructura \_ [**\_ MCI SEEK \_ PARMS.**](mci-seek-parms.md) Si usa el **miembro dwTo** para especificar una posición de búsqueda con MCI SEEK, debe consultar el formato de hora y \_ establecerlo, si es necesario.

Además de especificar una posición con el miembro **dwTo,** puede especificar las marcas MCI SEEK TO START o MCI SEEK TO END para el parámetro dwParam1 de la función \_ \_ \_ \_ \_ \_ [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))  para buscar las posiciones inicial y final del elemento de dispositivo. Si usa una de estas marcas, no especifique la marca MCI \_ TO.

 

 