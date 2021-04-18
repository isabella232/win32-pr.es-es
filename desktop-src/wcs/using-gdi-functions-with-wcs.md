---
title: Uso de funciones de GDI con WCS
description: Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que utilizan o operan en los datos de color.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Sistema de color de Windows (WCS), interfaz de dispositivo gráfico (GDI)
- WCS (sistema de color de Windows), interfaz de dispositivo gráfico (GDI)
- Administración del color de imagen, interfaz de dispositivo gráfico (GDI)
- Administración del color, interfaz de dispositivo gráfico (GDI)
- colores, interfaz de dispositivo gráfico (GDI)
- interfaz de dispositivo gráfico (GDI)
- GDI (interfaz de dispositivo gráfico)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f411d5d91c36bf5d2f2fa82f332c9b15519d800d
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105720784"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso de funciones de GDI con WCS

Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que utilizan o operan en los datos de color. Algunos están habilitados para su uso con WCS y otros no. Las siguientes funciones GDI son relevantes para ICM:

-   [Funciones de contexto de dispositivo con WCS](#device-context-functions-with-wcs)
-   [Funciones Pen y Brush con WCS](#pen-and-brush-functions-with-wcs)
-   [Funciones de salida de texto con WCS](#text-output-functions-with-wcs)
-   [Funciones de mapa de bits con WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funciones de contexto de dispositivo con WCS



|                    |                                                                                                                                                                                                                                 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | Si el contexto de dispositivo (DC) que se pasa a esta función a través de su parámetro HDC está habilitado para ICM, el controlador de dominio que crea la función también está habilitado para ICM. Los espacios de colores de origen y destino se especifican en el controlador de dominio. |
| CreateDC           | ICM se puede habilitar estableciendo el miembro dmICMMethod de la estructura DEVMODE señalada por el parámetro pInitData en el valor adecuado. Para obtener más información, consulte la documentación del SDK de la plataforma en la estructura DEVMODE.  |
| ResetDC            | El perfil de color del contexto de dispositivo especificado por el parámetro HDC se restablecerá en función de la información de la estructura DEVMODE especificada por el parámetro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funciones Pen y Brush con WCS



|                 |                                                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funciones de pincel | No se realiza ninguna administración de color al crear el pincel. Sin embargo, la administración del color se realizará cuando se seleccione el pincel en un controlador de dominio habilitado para ICM. |
| CreatePen       | No se realiza ninguna administración de color al crear el lápiz. Sin embargo, la administración del color se realizará cuando se seleccione el pincel en un controlador de dominio habilitado para ICM.   |
| ExtCreatePen    | No se realiza ninguna administración de color al crear el lápiz. Sin embargo, la administración del color se realizará cuando se seleccione el pincel en un controlador de dominio habilitado para ICM.   |
| SelectObject    | Si el objeto que se selecciona es un pincel o un lápiz, se realiza la administración del color.                                                              |
| SetDCBrushColor | La administración del color se realiza si se habilita WCS.                                                                                              |
| SetDCPenColor   | La administración del color se realiza si se habilita WCS.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funciones de salida de texto con WCS



|              |                                                  |
|--------------|--------------------------------------------------|
| SetBkColor   | La administración del color se realiza si se habilita WCS. |
| SetTextColor | La administración del color se realiza si se habilita WCS. |



 

## <a name="bitmap-functions-with-wcs"></a>Funciones de mapa de bits con WCS



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBlt            | No se realiza ninguna administración de color cuando se produce blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | El parámetro fuUsage especifica que el miembro bmiColors de la estructura BITMAPINFO (a la que apunta el parámetro lpbmi o no contiene información de color. Si no es así, no se realiza ninguna administración de color para este mapa de bits. El mapa de bits debe usar la versión 4 o la versión 5 de la estructura BITMAPINFO (para que se habilite la administración del color. El contenido del mapa de bits resultante no coincide con el color después de crear el mapa de bits. |
| CreateDIBSection  | Si la estructura BITMAPINFO (pasada a través del parámetro PBMI no es la versión 4 o la versión 5, no se realiza ninguna administración del color. Si es la versión 4 o 5, la administración del color está habilitada y el espacio de colores especificado está asociado al mapa de bits.                                                                                                                                                                                                   |
| MaskBlt           | No se realiza ninguna administración de color cuando se produce blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Si el objeto es un mapa de bits creado con CreateDIBSection, se realiza la administración del color. El espacio de colores del mapa de bits se utiliza como espacio de colores de destino.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Se realiza la administración del color. Si la estructura BITMAPINFO (especificada no es la versión 4 o la versión 5, se usa el perfil de color del controlador de dominio actual como perfil de espacio de colores de origen. Si no tiene una, se utiliza el espacio sRGB. Si la estructura BITMAPINFO (especificada es la versión 4 o la versión 5, el perfil de espacio de colores especificado en el encabezado de mapa de bits se usa como perfil de espacio de colores de origen.                                         |
| SetDIBitsToDevice | Se realiza la administración del color. Si la estructura BITMAPINFO (especificada no es la versión 4 o la versión 5, el perfil de color del contexto de dispositivo actual se usa como perfil de espacio de color de origen. Si no tiene una, se utiliza el espacio de color sRGB. Si la estructura BITMAPINFO (especificada es la versión 4 o la versión 5, el perfil de espacio de colores asociado al mapa de bits se utiliza como espacio de colores de origen.                                    |
| SetDIBColorTable  | No se realiza ninguna administración de color.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | No se realiza ninguna administración de color cuando se produce blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Se realiza la administración del color. Si la estructura BITMAPINFO (especificada no es la versión 4 o la versión 5, se usa el perfil de color del controlador de dominio actual como perfil de espacio de colores de origen. Si no tiene una, se utiliza el espacio sRGB. Si la estructura BITMAPINFO (especificada es la versión 4 o la versión 5, el perfil de espacio de colores especificado en el encabezado de mapa de bits se usa como perfil de espacio de colores de origen.                                         |



 

 

 




