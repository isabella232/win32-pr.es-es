---
description: Uniscribe guarda asignaciones de Unicode a glifo (cmap), anchos de glifo y tablas de modelado de scripts OpenType.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Almacenamiento en caché (internacionalización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d8444fa222c2b6f6c7b03d0e1be70c1e04b1509ab020b8769d87b2b5cbc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500835"
---
# <a name="caching-internationalization"></a>Almacenamiento en caché (internacionalización)

Uniscribe guarda asignaciones de Unicode a glifo (cmap), anchos de glifo y tablas de modelado de scripts OpenType. Un identificador de las tablas para una fuente determinada de un tamaño determinado se denomina "caché de scripts". Muchas funciones uniscribe llaman a para un parámetro de identificador de contexto de dispositivo y un puntero a una [**estructura DE \_ SCRIPT CACHE.**](script-cache.md) Estas funciones buscan primero información a través de la caché de scripts, usando el contexto del dispositivo solo cuando las tablas necesarias no están ya almacenadas en caché. Al llamar a [**la función ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)o [**ScriptTextOut,**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) la aplicación debe pasar un puntero a una **estructura SCRIPT \_ CACHE.** El identificador se debe inicializar en **NULL antes** de la primera vez que la aplicación lo pasa a una función uniscribe. La aplicación nunca debe pasar el mismo identificador para diferentes fuentes o tamaños diferentes.

Una aplicación puede liberar una caché de scripts en cualquier momento. Uniscribe mantiene los recuentos de referencias en sus cachés de fuente y formador, libera los datos de fuente solo cuando se liberan todos los tamaños de la fuente y libera los datos del formador solo cuando se liberan todas las fuentes que admite el formador. Cuando la aplicación se realiza con un estilo, debe llamar a la [**función ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) para liberar la caché de scripts para el estilo.

Para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) y [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), es válido que la aplicación pase un contexto de dispositivo null. La mayoría de las veces la llamada se realizará correctamente, ya que las tablas necesarias ya están almacenadas en caché. Si la forma o la selección de ubicación requieren acceso a un contexto de dispositivo, **ScriptShape** o **ScriptPlace** devuelve inmediatamente con el código de error E \_ PENDING. A continuación, la aplicación debe seleccionar la fuente en el contexto del dispositivo. Para la mayoría de las aplicaciones, esto ayuda al rendimiento al evitar la preparación repetida de un identificador de contexto de dispositivo con llamadas a [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
