---
title: Menús contextuales
description: Menús contextuales
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Reproductor de Windows Media en línea, menús contextuales
- tiendas en línea, menús contextuales
- tipo 1 tiendas en línea, menús contextuales
- Reproductor de Windows Media en línea, menús contextuales personalizados
- tiendas en línea, menús contextuales personalizados
- tipo 1 tiendas en línea, menús contextuales personalizados
- menús contextuales
- menús contextuales personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ad3bba5863f83b5f324821ec0904e7ef4c5881c7f10b9214eebde1081b217d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119354"
---
# <a name="context-menus"></a>Menús contextuales

Las tiendas en línea pueden proporcionar menús contextuales personalizados. Para ello, el complemento de la tienda en línea implementa el [método IWMPContentPartner::GetCommands.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) Reproductor de Windows Media llama a este método para proporcionar información sobre la ubicación en la interfaz de usuario donde se muestra el menú contextual (donde el usuario hizo clic con el botón derecho). El complemento devuelve una matriz de estructuras [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que describen cada elemento de menú contextual, incluido un identificador de comando para cada uno.

Una Reproductor de Windows Media recupera la matriz, el reproductor usa la matriz para compilar el menú contextual que el usuario ve. Cuando el usuario hace clic en un elemento en el menú contextual, el reproductor llama a [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)y pasa el identificador de comando asociado al elemento de menú a través del *parámetro dwCommandID.* El reproductor también pasa un valor de ubicación de biblioteca y una matriz de los IDs que representa los elementos en los que se invocó el menú, como una matriz de los IDs de pista. Con esta información, el complemento puede iniciar cualquier proceso adecuado en respuesta al clic del mouse del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




