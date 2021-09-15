---
title: Elegir cuándo crear objetos accesibles
description: Los desarrolladores de servidores pueden crear todos los objetos accesibles dentro de un contenedor cuando se crea el contenedor, o pueden crear los objetos accesibles dinámicamente.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466128"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Elegir cuándo crear objetos accesibles

Los desarrolladores de servidores pueden crear todos los objetos accesibles dentro de un contenedor cuando se crea el contenedor, o pueden crear los objetos accesibles dinámicamente.

Por ejemplo, imagine un cuadro de diálogo con varios controles personalizados. Un servidor crea objetos accesibles para todos los controles personalizados cuando se muestra el cuadro de diálogo. Sin embargo, si uno de los controles es un cuadro combinado personalizado, el servidor espera hasta que un usuario lo selecciona para crear objetos accesibles para los elementos que contiene el cuadro combinado.

Al hacer que el elemento primario cree objetos accesibles dinámicamente, las aplicaciones usan menos memoria que si todos los objetos accesibles posibles se crearon con antelación.

 

 




