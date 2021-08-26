---
description: Un contexto de dispositivo (DC) es una estructura de datos que define los objetos gráficos, sus atributos asociados y los modos gráficos que afectan a la salida en un dispositivo. Para crear un controlador de dominio, llame a la función CreateDC; para recuperar un controlador de dominio, llame a la función GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Mapas de bits, contextos de dispositivo y superficies de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed42215dc98ce179f9d36ddc0a24244c018c4177287d1fdfff974a2814e14d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966395"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Mapas de bits, contextos de dispositivo y superficies de dibujo

Un *contexto de dispositivo* (DC) es una estructura de datos que define los objetos gráficos, sus atributos asociados y los modos gráficos que afectan a la salida en un dispositivo. Para crear un controlador de dominio, llame a la [**función CreateDC;**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) para recuperar un controlador de dominio, llame a la [**función GetDC.**](/windows/desktop/api/Winuser/nf-winuser-getdc)

Antes de devolver un identificador que identifica ese controlador de dominio, el sistema selecciona una superficie de dibujo en el controlador de dominio. Si la aplicación llamó a la función [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) para crear un contexto de dispositivo para una pantalla VGA, las dimensiones de esta superficie de dibujo son de 640 a 480 píxeles. Si la aplicación llamó [**a la función GetDC,**](/windows/desktop/api/Winuser/nf-winuser-getdc) las dimensiones reflejan el tamaño del área cliente.

Para que una aplicación pueda empezar a dibujar, debe seleccionar un mapa de bits con el ancho y alto adecuados en el controlador de dominio mediante una llamada a [**la función SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Cuando una aplicación pasa el identificador al controlador de dominio a una de las funciones de dibujo de la interfaz de dispositivo gráfico (GDI), la salida solicitada aparece en la superficie de dibujo seleccionada en el controlador de dominio.

Para obtener más información, vea [Contextos de dispositivo de memoria.](memory-device-contexts.md)

 

 



