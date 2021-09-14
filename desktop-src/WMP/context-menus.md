---
title: Menús contextuales
description: Menús contextuales
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Reproductor de Windows Media en línea,menús contextuales
- tiendas en línea, menús contextuales
- tiendas en línea de tipo 1, menús contextuales
- Reproductor de Windows Media en línea, menús contextuales personalizados
- tiendas en línea, menús contextuales personalizados
- tiendas en línea de tipo 1, menús contextuales personalizados
- menús contextuales
- menús contextuales personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967731"
---
# <a name="context-menus"></a>Menús contextuales

Las tiendas en línea pueden proporcionar menús contextuales personalizados. Para ello, el complemento de tienda en línea implementa el [método IWMPContentPartner::GetCommands.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) Reproductor de Windows Media llama a este método para proporcionar información sobre la ubicación en la interfaz de usuario donde se muestra el menú contextual (donde el usuario hizo clic con el botón derecho). El complemento devuelve una matriz de estructuras [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que describen cada elemento de menú contextual, incluido un identificador de comando para cada uno.

Una Reproductor de Windows Media recupera la matriz, el reproductor usa la matriz para compilar el menú contextual que el usuario ve. Cuando el usuario hace clic en un elemento en el menú contextual, el Reproductor llama a [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)y pasa el identificador de comando asociado al elemento de menú a través del *parámetro dwCommandID.* El reproductor también pasa un valor de ubicación de biblioteca y una matriz de los iDs que representa los elementos en los que se invocó el menú, como una matriz de los ID de pista. Con esta información, el complemento puede iniciar cualquier proceso adecuado en respuesta al clic del mouse del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




