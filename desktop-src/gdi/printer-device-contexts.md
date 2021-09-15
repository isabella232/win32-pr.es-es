---
description: El controlador de dominio de la impresora se puede usar al imprimir en una impresora de matriz de puntos, impresora ink-jet, impresora de rayos o trazador.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contextos de dispositivo de impresora (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360471"
---
# <a name="printer-device-contexts-windows-gdi"></a>Contextos de dispositivo de impresora (Windows GDI)

El controlador de dominio de la impresora se puede usar al imprimir en una impresora de matriz de puntos, impresora ink-jet, impresora de rayos o trazador. Una aplicación crea un controlador de dominio de impresora llamando a la función [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) y suministrando los argumentos adecuados (el nombre del controlador de impresora, el nombre de la impresora, el archivo o el nombre del dispositivo para el medio de salida físico y otros datos de inicialización). Cuando una aplicación ha terminado de imprimir, elimina el controlador de dominio de la impresora mediante una llamada a la [**función DeleteDC.**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) Una aplicación debe eliminar (en lugar de liberar) un controlador de dominio de impresora; Se produce un error en la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) cuando una aplicación intenta usarla para liberar un controlador de dominio de impresora.

Para obtener más información, vea [Salida de impresora.](../printdocs/printer-output.md)

 

 
