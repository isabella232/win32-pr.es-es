---
title: Menús contextuales
description: Menús contextuales
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player tiendas en línea, menús contextuales
- tiendas en línea, menús contextuales
- tipo 1 tiendas en línea, menús contextuales
- Windows Media Player tiendas en línea, menús contextuales personalizados
- tiendas en línea, menús contextuales personalizados
- tipo 1 almacenes en línea, menús contextuales personalizados
- menús contextuales
- menús contextuales personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420231"
---
# <a name="context-menus"></a>Menús contextuales

Las tiendas en línea pueden proporcionar menús contextuales personalizados. Para ello, el complemento de la tienda en línea implementa el método [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) . Windows Media Player llama a este método para proporcionar información sobre la ubicación en la interfaz de usuario en la que se muestra el menú contextual (donde el usuario hizo clic con el botón secundario). El complemento devuelve una matriz de estructuras [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que describen cada elemento de menú contextual, incluido un identificador de comando para cada uno.

Una vez que Windows Media Player ha recuperado la matriz, el reproductor utiliza la matriz para crear el menú contextual que el usuario ve. Cuando el usuario hace clic en un elemento en el menú contextual, el reproductor llama a [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), pasando el identificador de comando asociado al elemento de menú mediante el parámetro *dwCommandID* . El reproductor también pasa un valor de ubicación de la biblioteca y una matriz de identificadores que representa los elementos en los que se invocó el menú, como una matriz de identificadores de seguimiento. Con esta información, el complemento puede iniciar cualquier proceso adecuado en respuesta al clic del mouse del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




