---
description: El sistema mantiene una caché de contextos de dispositivo de visualización que usa para contextos de dispositivo comunes, primarios y de ventana.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Mostrar caché de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581132"
---
# <a name="display-device-context-cache"></a>Mostrar caché de contexto de dispositivo

El sistema mantiene una caché de contextos de dispositivo de visualización que usa para contextos de dispositivo comunes, primarios y de ventana. El sistema recupera un contexto de dispositivo de la memoria caché cada vez que una aplicación llama a la [**función GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**BeginPaint;**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) el sistema devuelve el controlador de dominio a la memoria caché cuando la aplicación llama posteriormente a la [**función ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) [**o EndPaint.**](/windows/desktop/api/Winuser/nf-winuser-endpaint)

No hay ningún límite predeterminado en la cantidad de contextos de dispositivo que puede contener una memoria caché. El sistema crea un nuevo contexto de dispositivo de presentación para la memoria caché si no hay ninguno disponible. Dado esto, una aplicación puede tener más de cinco contextos de dispositivo activos desde la memoria caché a la vez. Sin embargo, la aplicación debe seguir liberando estos contextos de dispositivo después de su uso. Dado que los nuevos contextos de dispositivo de visualización para la memoria caché se asignan en el espacio del montón de la aplicación, si no se liberan los contextos del dispositivo, se consume todo el espacio del montón disponible. El sistema indica este error devolviendo un error cuando no puede asignar espacio para el nuevo contexto de dispositivo. Otras funciones no relacionadas con la memoria caché también pueden devolver errores.

 

 



