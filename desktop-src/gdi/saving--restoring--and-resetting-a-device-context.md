---
description: 'Las siguientes funciones permiten que una aplicación guarde, restaure y restablezca un contexto de dispositivo: SaveDC, RestoreDC y ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Guardar, restaurar y restablecer un contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434ef484fecee17251a31616e396ee0fa66b381bc30cf858575f4455ca36a1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965255"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Guardar, restaurar y restablecer un contexto de dispositivo

Las siguientes funciones permiten que una aplicación guarde, restaure y restablezca un contexto de dispositivo: [**SaveDC,**](/windows/desktop/api/Wingdi/nf-wingdi-savedc) [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)y [**ResetDC.**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) La función SaveDC registra en una pila GDI especial los objetos gráficos del controlador de dominio actual, sus atributos y modos gráficos. Una aplicación de dibujo puede llamar a esta función antes de que un usuario comience a dibujar y guardar el estado original de la aplicación proporcionando una pizarra limpia para el usuario. Para volver a este estado original, la aplicación llama a la función RestoreDC.

[**ResetDC se**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) proporciona para restablecer los datos del controlador de dominio de la impresora. Una aplicación llama a esta función para restablecer la orientación del papel, el tamaño del papel, el factor de escalado de salida, el número de copias que se imprimirán, el origen del papel (o bin), el modo dúplex, y así sucesivamente. Normalmente, una aplicación llama a esta función después de que un usuario haya cambiado una de las opciones de impresora y el sistema haya emitido un [**mensaje \_ WM DEVMODECHANGE.**](wm-devmodechange.md)

 

 



