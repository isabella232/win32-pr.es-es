---
title: Asignación de código Visual Basic ADSI a código de C++
description: ADSI consta de más de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172178"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Asignación de código Visual Basic ADSI a código de C++

ADSI consta de más de 50 interfaces. La mayoría de las operaciones de directorio se pueden completar con solo cinco interfaces. Son las siguientes:

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

En la tabla siguiente se enumeran las asignaciones del código ADSI VB/VBS al código de C++. Tenga en cuenta que esta no es una lista completa.



| Código VBS                           | Código VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject()              | hr = AdsGetObject()                                                   |
| Obj. Coloque obj. Obtiene obj. Padre         | IADs o IDirectoryObject                                              |
| Obj. Cree obj. Eliminar obj. MoveHere | IADsContainer                                                         |
| Para cada... En...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Connection, Command, RecordSet     | IDirectorySearch                                                      |
| Descriptor de seguridad, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




