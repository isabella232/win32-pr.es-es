---
description: 'Hay dos tipos de pinceles: lógico y físico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Acerca de los pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155212"
---
# <a name="about-brushes"></a>Acerca de los pinceles

Hay dos tipos de pinceles: lógico y físico. Un *pincel lógico* es una descripción del mapa de bits ideal que una aplicación usa para pintar formas. Un *pincel físico* es el mapa de bits real que un controlador de dispositivo crea en función de la definición de pincel lógico de una aplicación. Para obtener más información sobre los mapas de bits, vea [mapas de bits](bitmaps.md).

Cuando una aplicación llama a una de las funciones que crea un pincel, recupera un identificador que identifica un pincel lógico. Cuando la aplicación pasa este identificador a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , el controlador de dispositivo de la pantalla o impresora correspondiente crea el pincel físico.

En los temas siguientes se describen los pinceles:

-   [Origen del pincel](brush-origin.md)
-   [Tipos de pinceles lógicos](logical-brush-types.md)
-   [Transferencia de bloque de patrón](pattern-block-transfer.md)
-   [Funciones de pincel habilitadas para ICM](icm-enabled-brush-functions.md)

 

 



