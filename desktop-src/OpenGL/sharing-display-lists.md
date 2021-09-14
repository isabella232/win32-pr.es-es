---
title: Compartir listas de visualización
description: Cuando se crea un contexto de representación, tiene su propio espacio para mostrar.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL on Windows,sharing display lists
- compartir listas de visualización OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069269"
---
# <a name="sharing-display-lists"></a>Compartir listas de visualización

Cuando se crea un contexto de representación, tiene su propio espacio para mostrar. La [**función wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permite que un contexto de representación comparta el espacio de la lista de presentación de otro contexto de representación. Cualquier número de contextos de representación puede compartir un único espacio para mostrar.

 

 




