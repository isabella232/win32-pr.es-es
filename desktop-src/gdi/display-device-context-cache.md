---
description: El sistema mantiene una caché de los contextos de dispositivo de pantalla que usa para los contextos de dispositivo comunes, primarios y de Windows.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Mostrar caché de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997409"
---
# <a name="display-device-context-cache"></a>Mostrar caché de contexto de dispositivo

El sistema mantiene una caché de los contextos de dispositivo de pantalla que usa para los contextos de dispositivo comunes, primarios y de Windows. El sistema recupera un contexto de dispositivo de la memoria caché cada vez que una aplicación llama a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; el sistema devuelve el controlador de dominio a la memoria caché cuando la aplicación llama posteriormente a la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) o [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

No hay ningún límite predeterminado en la cantidad de contextos de dispositivo que puede contener una memoria caché; el sistema crea un nuevo contexto de dispositivo de pantalla para la memoria caché si no hay ninguno disponible. Dado esto, una aplicación puede tener más de cinco contextos de dispositivo activos de la memoria caché a la vez. Sin embargo, la aplicación debe continuar lanzando estos contextos de dispositivo después del uso. Dado que se asignan nuevos contextos de dispositivo de pantalla para la memoria caché en el espacio de montón de la aplicación, si no se liberan los contextos de dispositivo, se consume todo el espacio de montón disponible. El sistema indica este error devolviendo un error cuando no se puede asignar espacio para el nuevo contexto de dispositivo. Otras funciones no relacionadas con la memoria caché también pueden devolver errores.

 

 



