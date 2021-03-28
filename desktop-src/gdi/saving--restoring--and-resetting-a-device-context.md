---
description: 'Las siguientes funciones permiten a una aplicación guardar, restaurar y restablecer un contexto de dispositivo: SaveDC, RestoreDC y ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Guardar, restaurar y restablecer un contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985555"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Guardar, restaurar y restablecer un contexto de dispositivo

Las siguientes funciones permiten a una aplicación guardar, restaurar y restablecer un contexto de dispositivo: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)y [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca). La función SaveDC registra en una pila de GDI especial los objetos gráficos del controlador de dominio actual y sus atributos, y los modos gráficos. Una aplicación de dibujo puede llamar a esta función antes de que un usuario empiece a dibujar y guardar el estado original de la aplicación proporcionando una pizarra limpia para el usuario. Para volver a este estado original, la aplicación llama a la función RestoreDC.

Se proporciona [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) para restablecer los datos de DC de la impresora. Una aplicación llama a esta función para restablecer la orientación del papel, el tamaño del papel, el factor de escala de salida, el número de copias que se van a imprimir, el origen del papel (o la ubicación), el modo dúplex, etc. Normalmente, una aplicación llama a esta función después de que un usuario ha cambiado una de las opciones de la impresora y el sistema ha emitido un mensaje de [**\_ DEVMODECHANGE de WM**](wm-devmodechange.md) .

 

 



