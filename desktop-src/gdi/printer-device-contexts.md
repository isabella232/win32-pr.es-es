---
description: El controlador de dominio de impresora se puede usar al imprimir en una impresora de matriz de puntos, una impresora de inyección de tinta, una impresora láser o un trazador.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contextos de dispositivo de impresora (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984854"
---
# <a name="printer-device-contexts-windows-gdi"></a>Contextos de dispositivo de impresora (Windows GDI)

El controlador de dominio de impresora se puede usar al imprimir en una impresora de matriz de puntos, una impresora de inyección de tinta, una impresora láser o un trazador. Una aplicación crea un controlador de dominio de impresora mediante una llamada a la función [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) y proporcionando los argumentos adecuados (el nombre del controlador de impresora, el nombre de la impresora, el nombre de archivo o dispositivo para el medio de salida físico y otros datos de inicialización). Cuando una aplicación ha terminado de imprimirse, elimina el controlador de dominio de la impresora mediante una llamada a la función [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) . Una aplicación debe eliminar (en lugar de liberar) un controlador de dominio de impresora; se produce un error en la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) cuando una aplicación intenta utilizarla para liberar un controlador de dominio de impresora.

Para obtener más información, consulte la salida de la [impresora](../printdocs/printer-output.md).

 

 
