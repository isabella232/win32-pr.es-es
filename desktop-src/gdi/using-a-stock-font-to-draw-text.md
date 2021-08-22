---
description: El sistema proporciona seis fuentes estándar.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Usar una fuente estándar para dibujar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9bd140a931a13f6232235036fb7b9cf3de1a20505666e869f214219b7a60a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468335"
---
# <a name="using-a-stock-font-to-draw-text"></a>Usar una fuente estándar para dibujar texto

El sistema proporciona seis fuentes estándar. Una fuente estándar es una fuente lógica que una aplicación puede obtener llamando a la [función GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) y especificando la fuente solicitada. La lista siguiente contiene los valores que puede especificar para obtener una fuente estándar.



| Value                 | Significado                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANSI \_ FIXED \_ FONT     | Especifica una fuente monoespacial basada en el Windows de caracteres. Normalmente se usa una fuente Courier.                                                                                                                                                                                                |
| ANSI \_ VAR \_ FONT       | Especifica una fuente proporcional basada en el juego Windows caracteres. Normalmente se usa MS Sans Serif.                                                                                                                                                                                              |
| FUENTE \_ PREDETERMINADA DEL \_ DISPOSITIVO | Especifica la fuente preferida para el dispositivo especificado. Suele ser la fuente System para los dispositivos de visualización. sin embargo, para algunas impresoras de matriz de puntos, se trata de una fuente que se encuentra en el dispositivo. (La impresión con esta fuente suele ser más rápida que imprimir con una fuente de mapa de bits descargada).    |
| FUENTE \_ FIJA DE \_ OEM      | Especifica una fuente monoespacial basada en un juego de caracteres OEM. Para equipos IBM y compatibles, la fuente OEM se basa en el juego de caracteres de PC de IBM.                                                                                                                                                 |
| FUENTE DEL \_ SISTEMA          | Especifica la fuente System. Se trata de una fuente proporcional basada en el juego de caracteres Windows y lo usa el sistema operativo para mostrar títulos de ventana, nombres de menú y texto en cuadros de diálogo. La fuente System siempre está disponible. Otras fuentes solo están disponibles si se han instalado. |
| FUENTE \_ FIJA DEL \_ SISTEMA   | Especifica una fuente monoespacial compatible con la fuente System en las primeras versiones de Windows.                                                                                                                                                                                                        |



 

Para obtener más información sobre las fuentes, vea [Acerca de las fuentes](about-fonts.md).

En el ejemplo siguiente se recupera un identificador de la fuente estándar variable, se selecciona en un contexto de dispositivo y, a continuación, se escribe una cadena con esa fuente:


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



Si no hay otras fuentes estándar disponibles, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) devuelve un identificador a la fuente System (SYSTEM \_ FONT). Solo debe usar fuentes estándar si el modo de asignación para el contexto de dispositivo de la aplicación es MM \_ TEXT.

 

 



