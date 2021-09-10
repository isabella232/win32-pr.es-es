---
title: Generación de Four-Character de datos
description: Generación de Four-Character de datos
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- E/S de archivos multimedia, códigos de cuatro caracteres
- E/S de archivo, códigos de cuatro caracteres
- entrada y salida (E/S), códigos de cuatro caracteres
- E/S (entrada y salida), códigos de cuatro caracteres
- códigos de cuatro caracteres
- Función mmioStringToFOURCC
- macro mmioFOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371810"
---
# <a name="generating-four-character-codes"></a>Generación de Four-Character de datos

Puede usar la [**macro mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) o la función [**mmioStringToFOURCC para**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) generar códigos de cuatro caracteres. En el ejemplo siguiente se **usa mmioFOURCC para** generar un código de cuatro caracteres para "WAVE".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



En el ejemplo siguiente se [**usa mmioStringToFOURCC para**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) generar un código de cuatro caracteres para "WAVE".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



El segundo parámetro de [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) especifica marcas para convertir la cadena en un código de cuatro caracteres. Si especifica la marca MMIO \_ TOUPPER, **mmioStringToFOURCC** convierte todos los caracteres alfabéticos de la cadena a mayúsculas. Esto resulta útil cuando es necesario especificar un código de cuatro caracteres para identificar un procedimiento de E/S personalizado, ya que los códigos de cuatro caracteres que identifican los nombres de extensión de archivo deben estar en mayúsculas.

 

 