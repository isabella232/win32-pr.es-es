---
description: Uniscribe guarda las asignaciones de Unicode a glifo (CMAP), los anchos del glifo y las tablas de forma de script OpenType.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Almacenamiento en caché (internacionalización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf8bf7dd10fe414bc170086ff9b8c34142dc197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689566"
---
# <a name="caching-internationalization"></a>Almacenamiento en caché (internacionalización)

Uniscribe guarda las asignaciones de Unicode a glifo (CMAP), los anchos del glifo y las tablas de forma de script OpenType. Un identificador de las tablas para una fuente determinada de un tamaño determinado se denomina "caché de script". Muchas funciones de Uniscribe llaman para un parámetro de identificador de contexto de dispositivo y un puntero a una estructura de [**\_ caché de scripts**](script-cache.md) . Estas funciones buscan primero información a través de la caché de scripts, usando el contexto de dispositivo solo cuando las tablas necesarias no están almacenadas en caché. Cuando se llama a la función [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)o [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) , la aplicación debe pasar un puntero a una estructura de **\_ caché de script** . El identificador se debe inicializar en **null** antes de la primera vez que la aplicación lo pasa a una función de Uniscribe. La aplicación nunca debe pasar el mismo identificador para diferentes fuentes o tamaños diferentes.

Una aplicación puede liberar una memoria caché de script en cualquier momento. Mantiene los recuentos de referencias en las memorias caché de la fuente y el forma, libera los datos de fuente solo cuando se liberan todos los tamaños de la fuente y libera los datos del mismo nivel solo cuando se liberan todas las fuentes que admite el forma. Cuando la aplicación se realiza con un estilo, debe llamar a la función [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) para liberar la memoria caché del script para el estilo.

Para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) y [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), es válido para la aplicación pasar un contexto de dispositivo nulo. Lo más frecuente es que la llamada se realice correctamente, ya que las tablas necesarias ya están almacenadas en caché. Si el modelado o la selección de ubicación requiere acceso a un contexto de dispositivo, **ScriptShape** o **ScriptPlace** devuelven inmediatamente con el \_ código de error E pendiente. A continuación, la aplicación debe seleccionar la fuente en el contexto del dispositivo. Para la mayoría de las aplicaciones, esto ayuda al rendimiento evitando la preparación repetida de un identificador de contexto de dispositivo con llamadas a [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
