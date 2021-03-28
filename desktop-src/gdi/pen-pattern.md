---
description: El atributo Pattern especifica el patrón de una pluma geométrica.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Patrón de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544422"
---
# <a name="pen-pattern"></a>Patrón de lápiz

El atributo Pattern especifica el patrón de una pluma geométrica.

En la ilustración siguiente se muestran líneas dibujadas con diferentes lápices geométricos. Cada lápiz se creó con un atributo de patrón diferente.

![Ilustración que muestra cuatro líneas, cada una con un lápiz diferente](images/cspen-02.png)

La primera línea de la ilustración anterior se dibuja utilizando uno de los seis patrones de trama disponibles; para obtener más información sobre los patrones de trama, vea [sombreado de lápiz](pen-hatch.md). La línea siguiente se dibuja con el patrón hueco, idéntico al patrón null. La tercera línea se dibuja mediante un patrón personalizado creado a partir de un mapa de bits de 8 por 8 píxeles. (Para obtener más información sobre los mapas de bits y su creación, vea [mapas de bits](bitmaps.md)). La última línea se dibuja con un patrón sólido. Al crear un pincel y pasar su identificador a la función [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) , se crea un modelo.

 

 



