---
title: Elegir cuándo crear objetos accesibles
description: Los desarrolladores de servidores pueden crear todos los objetos accesibles dentro de un contenedor cuando se crea el contenedor, o bien pueden crear los objetos accesibles dinámicamente.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a53ee02cb7de574242b3ba9986cdf0ce6068e8495e1ebaf638eed08e9c04b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325984"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Elegir cuándo crear objetos accesibles

Los desarrolladores de servidores pueden crear todos los objetos accesibles dentro de un contenedor cuando se crea el contenedor, o bien pueden crear los objetos accesibles dinámicamente.

Por ejemplo, imagine un cuadro de diálogo con varios controles personalizados. Un servidor crea objetos accesibles para todos los controles personalizados cuando se muestra el cuadro de diálogo. Sin embargo, si uno de los controles es un cuadro combinado personalizado, el servidor espera hasta que un usuario lo selecciona para crear objetos accesibles para los elementos que contiene el cuadro combinado.

Al hacer que el elemento primario cree objetos accesibles dinámicamente, las aplicaciones usan menos memoria que si todos los objetos accesibles posibles se crearon con antelación.

 

 




