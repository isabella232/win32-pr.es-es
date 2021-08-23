---
description: 'Hay dos tipos de pinceles: lógico y físico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Acerca de los pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c94ea9dac021a013ccc4ef624f9b00a3234102ac905999cb7c085148be91b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602801"
---
# <a name="about-brushes"></a>Acerca de los pinceles

Hay dos tipos de pinceles: lógico y físico. Un *pincel lógico es* una descripción del mapa de bits ideal que una aplicación usa para pintar formas. Un *pincel físico* es el mapa de bits real que un controlador de dispositivo crea en función de la definición de pincel lógico de una aplicación. Para obtener más información sobre los mapas de bits, vea [Mapas de bits.](bitmaps.md)

Cuando una aplicación llama a una de las funciones que crea un pincel, recupera un identificador que identifica un pincel lógico. Cuando la aplicación pasa este identificador a la [**función SelectObject,**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) el controlador de dispositivo para la pantalla o impresora correspondientes crea el pincel físico.

En los temas siguientes se describen los pinceles:

-   [Origen del pincel](brush-origin.md)
-   [Tipos de pincel lógicos](logical-brush-types.md)
-   [Transferencia de bloques de patrones](pattern-block-transfer.md)
-   [ICM funciones de pincel habilitadas para el usuario](icm-enabled-brush-functions.md)

 

 



