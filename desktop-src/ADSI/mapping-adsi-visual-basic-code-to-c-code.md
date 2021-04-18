---
title: Asignación de código ADSI Visual Basic a código de C++
description: ADSI consta de más de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656164"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Asignación de código ADSI Visual Basic a código de C++

ADSI consta de más de 50 interfaces. La mayoría de las operaciones de directorio se pueden completar con solo cinco interfaces. Son las siguientes:

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

En la tabla siguiente se enumeran las asignaciones de código ADSI VB/VBS a código de C++. Tenga en cuenta que esta no es una lista completa.



| Código VBS                           | Código VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = AdsGetObject ()                                                   |
| obj. Put obj. Obtener obj. Aérea         | IADs o IDirectoryObject                                              |
| obj. Crear obj. Eliminar obj. MoveHere | IADsContainer                                                         |
| Para cada... en...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Conexión, comando, conjunto de registros     | IDirectorySearch                                                      |
| Descriptor de seguridad, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




