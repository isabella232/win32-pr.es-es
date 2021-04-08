---
title: Mover objetos
description: Mover objetos
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, mover objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077509"
---
# <a name="moving-objects"></a>Mover objetos

Para trasladar un objeto dentro de un dominio, use el método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

**Para desplace un objeto dentro de un dominio**

1.  Enlazar a la interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) del objeto que se va a trasladar.
2.  Obtiene el ADsPath del objeto que se va a desplace de la propiedad [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .
3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del contenedor al que se va a desplace el objeto.
4.  Mueva el objeto con el método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

Si existe una interfaz para el objeto que se ha despasado, la interfaz no es válida después de que el objeto se haya despuesto porque el objeto de directorio que la interfaz representa ya no existe.

Para obtener más información y un ejemplo de código que muestra cómo mover un objeto, vea el [código de ejemplo para mover un objeto](example-code-for-moving-an-object.md).

 

 