---
title: Operaciones de DrawDib
description: Operaciones de DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, acerca de
- DrawDib, acceso
- DrawDib, abrir
- DrawDib, operaciones
- DrawDib, contexto de dispositivo (DC)
- DC (contexto de dispositivo)
- DrawDibOpen función)
- DrawDibClose función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487038"
---
# <a name="drawdib-operations"></a>Operaciones de DrawDib

Puede tener acceso a todo el grupo de funciones de DrawDib mediante la función [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) . Esta función carga la biblioteca de vínculos dinámicos (DLL), asigna recursos de memoria, crea un contexto de dispositivo DrawDib (DC) y mantiene un recuento de referencias del número de controladores de dominio que se inicializan. **DrawDibOpen** también devuelve un identificador del nuevo controlador de dominio que se usa con las otras funciones de DrawDib.

Puede liberar un controlador de dominio de DrawDib cuando termine de usarlo mediante la función [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) . **DrawDibClose** también reduce el recuento de referencias de las aplicaciones que tienen acceso a la dll. La llamada a **DrawDibClose** debe ser la última función DrawDib de la aplicación.

Puede crear tantos controladores de usuario de DrawDib como desee. Puede usar varios controladores de usuario de DrawDib para dibujar varios mapas de bits simultáneamente. También puede crear varios controladores de dominio de DrawDib, cada uno con características únicas, de modo que la aplicación pueda elegir y usar el controlador de dominio con la configuración más adecuada. Por ejemplo, puede crear dos controladores de DrawDib en una aplicación: uno que muestre una imagen en su resolución normal y otro que muestre una parte ampliada de la imagen.

Para ejecutarse de forma eficaz, las funciones de DrawDib requieren información sobre el adaptador de pantalla y su controlador. El perfil de visualización se obtiene ejecutando una serie de pruebas en el adaptador de pantalla la primera vez que se tiene acceso a la DLL que contiene las funciones de DrawDib. Las funciones DrawDib usan esta información para todas las aplicaciones. Puede repetir estas pruebas cuando sea necesario mediante la función [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .

> [!Note]  
> Recuperar y almacenar el perfil de visualización suele ser una sola vez. No obstante, si se elimina la información de perfil u otro controlador de pantalla está instalado en el sistema, DrawDib vuelve a ejecutar las pruebas.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las funciones de DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




