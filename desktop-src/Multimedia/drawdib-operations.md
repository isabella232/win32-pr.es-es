---
title: Operaciones DrawDib
description: Operaciones DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib,about
- DrawDib,accessing
- DrawDib,opening
- DrawDib,operations
- DrawDib, contexto de dispositivo (DC)
- DC (contexto del dispositivo)
- Función DrawDibOpen
- Función DrawDibClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274052"
---
# <a name="drawdib-operations"></a>Operaciones DrawDib

Puede acceder a todo el grupo de funciones DrawDib mediante la [**función DrawDibOpen.**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) Esta función carga la biblioteca de vínculos dinámicos (DLL), asigna recursos de memoria, crea un contexto de dispositivo DrawDib (DC) y mantiene un recuento de referencias del número de dc que se inicializan. **DrawDibOpen también** devuelve un identificador del nuevo controlador de dominio que se usa con las otras funciones DrawDib.

Puede liberar un controlador de dominio DrawDib cuando termine de usarlo mediante la [**función DrawDibClose.**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) **DrawDibClose también** disminuye el recuento de referencias de las aplicaciones que acceden al archivo DLL. La llamada a **DrawDibClose** debe ser la última función DrawDib de la aplicación.

Puede crear tantos DCs DrawDib como desee. Puede usar varios DCs DrawDib para dibujar varios mapas de bits simultáneamente. También puede crear varios DC DrawDib, cada uno con características únicas, para que la aplicación pueda elegir y, a continuación, usar el controlador de dominio con la configuración más adecuada. Por ejemplo, puede crear dos DCs DrawDib en una aplicación: uno que muestra una imagen con su resolución normal y el otro que muestra una parte ampliada de la imagen.

Para ejecutarse de forma eficaz, las funciones DrawDib requieren información sobre el adaptador de pantalla y su controlador. El perfil de presentación se obtiene mediante la ejecución de una serie de pruebas en el adaptador de pantalla la primera vez que se tiene acceso al archivo DLL que contiene las funciones DrawDib. Las funciones DrawDib usan esta información para todas las aplicaciones. Puede repetir estas pruebas cuando sea necesario mediante la [**función DrawDibProfileDisplay.**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay)

> [!Note]  
> Recuperar y almacenar el perfil de presentación suele ser una repetición única. Sin embargo, si se elimina la información del perfil o se instala otro controlador de pantalla en el sistema, DrawDib vuelve a ejecutar las pruebas.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las funciones DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




