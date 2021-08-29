---
title: Compartir listas de visualización
description: Cuando se crea un contexto de representación, tiene su propio espacio para mostrar.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL on Windows,sharing display lists
- compartir listas de visualización OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934789f3de00e6e0be451fc441416dfcbaa057b0b58b224fc57021db31575e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776635"
---
# <a name="sharing-display-lists"></a>Compartir listas de visualización

Cuando se crea un contexto de representación, tiene su propio espacio para mostrar. La [**función wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permite que un contexto de representación comparta el espacio de la lista de presentación de otro contexto de representación. Cualquier número de contextos de representación puede compartir un único espacio para mostrar.

 

 




