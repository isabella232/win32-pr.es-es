---
title: Compartir listas de visualización
description: Cuando se crea un contexto de representación, tiene su propio espacio de lista de presentación.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL en Windows, compartir listas de visualización
- compartir listas de visualización OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357618"
---
# <a name="sharing-display-lists"></a>Compartir listas de visualización

Cuando se crea un contexto de representación, tiene su propio espacio de lista de presentación. La función [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permite a un contexto de representación compartir el espacio de la lista de presentación de otro contexto de representación. Cualquier número de contextos de representación puede compartir un solo espacio de lista de presentación.

 

 




