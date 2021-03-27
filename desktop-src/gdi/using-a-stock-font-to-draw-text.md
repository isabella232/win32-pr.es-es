---
description: El sistema proporciona seis fuentes estándar.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Usar una fuente estándar para dibujar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002731"
---
# <a name="using-a-stock-font-to-draw-text"></a>Usar una fuente estándar para dibujar texto

El sistema proporciona seis fuentes estándar. Una fuente estándar es una fuente lógica que una aplicación puede obtener llamando a la función [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) y especificando la fuente solicitada. La lista siguiente contiene los valores que se pueden especificar para obtener una fuente estándar.



| Value                 | Significado                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fuente ANSI fija \_     | Especifica una fuente monoespaciada basada en el juego de caracteres de Windows. Normalmente se utiliza una fuente Courier.                                                                                                                                                                                                |
| \_fuente ANSI var \_       | Especifica una fuente proporcional basada en el juego de caracteres de Windows. Normalmente se utiliza MS Sans Serif.                                                                                                                                                                                              |
| \_fuente predeterminada del dispositivo \_ | Especifica la fuente preferida para el dispositivo especificado. Suele ser la fuente del sistema para los dispositivos de visualización; sin embargo, para algunas impresoras matriciales se trata de una fuente que reside en el dispositivo. (La impresión con esta fuente suele ser más rápida que la impresión con una fuente de mapa de bits descargada).    |
| \_fuente fija \_ OEM      | Especifica una fuente monoespaciada basada en un juego de caracteres OEM. En el caso de los equipos de IBM y los compatibles, la fuente OEM se basa en el juego de caracteres de IBM PC.                                                                                                                                                 |
| fuente del sistema \_          | Especifica la fuente del sistema. Se trata de una fuente proporcional basada en el juego de caracteres de Windows y que el sistema operativo utiliza para mostrar los títulos de ventana, los nombres de menú y el texto en los cuadros de diálogo. La fuente del sistema siempre está disponible. Otras fuentes solo están disponibles si se han instalado. |
| \_fuente fija del sistema \_   | Especifica una fuente monoespaciada compatible con la fuente del sistema en versiones anteriores de Windows.                                                                                                                                                                                                        |



 

Para obtener más información sobre las fuentes, vea acerca de las [fuentes](about-fonts.md).

En el ejemplo siguiente se recupera un identificador de la fuente stock variable, se selecciona en un contexto de dispositivo y, a continuación, se escribe una cadena con esa fuente:


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



Si otras fuentes bursátiles no están disponibles, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) devuelve un identificador a la fuente del sistema (fuente del sistema \_ ). Solo debe usar fuentes estándar si el modo de asignación del contexto de dispositivo de la aplicación es \_ texto mm.

 

 



