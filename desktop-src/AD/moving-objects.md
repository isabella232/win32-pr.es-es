---
title: Mover objetos
description: Mover objetos
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos de Active Directory , mover objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1158bfc3fb85712b2ab52b6b69d86c7af52675d210b75b0c9974fc2da6359ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025863"
---
# <a name="moving-objects"></a>Mover objetos

Para mover un objeto dentro de un dominio, use [**el método IADsContainer.MoveHere.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

**Para mover un objeto dentro de un dominio**

1.  Enlace a la [**interfaz IAD del**](/windows/desktop/api/iads/nn-iads-iads) objeto que se moverá.
2.  Obtenga el valor de ADsPath del objeto que se moverá de la [**propiedad IADs.ADsPath.**](/windows/desktop/ADSI/iads-property-methods)
3.  Enlace a la [**interfaz IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del contenedor al que se va a mover el objeto.
4.  Mueva el objeto con [**el método IADsContainer.MoveHere.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Si existe una interfaz para el objeto que se ha movido, la interfaz no es válida después de mover el objeto porque el objeto de directorio que representa la interfaz ya no existe.

Para obtener más información y un ejemplo de código que muestra cómo mover un objeto, vea [Código de ejemplo para mover un objeto](example-code-for-moving-an-object.md).

 

 