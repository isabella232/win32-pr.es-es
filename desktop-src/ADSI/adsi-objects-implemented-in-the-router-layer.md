---
title: Objetos ADSI implementados en el nivel de enrutador
description: En la tabla siguiente se presenta una breve descripción de los objetos COM implementados en el enrutador ADSI.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fad496bbfea220dca0046cac40daf41120675
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418363"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>Objetos ADSI implementados en el nivel de enrutador

En la tabla siguiente se presenta una breve descripción de los objetos COM implementados en el enrutador ADSI.



| Objeto ADSI            | Descripción                                                         | Interfaces admitidas                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AccessControlEntry** | Objeto ADSI que representa una entrada de control de acceso (ACE).       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Objeto ADSI que representa una lista de control de acceso (ACL).        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **ADsNamespaces**      | Objeto ADSI que representa el contenedor de varios espacios de nombres. | <dl> <dt>[](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> de iAds de iAds </dl> |
| **LargeInteger**       | Objeto ADSI que representa un entero grande.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **PropertyEntry**      | Objeto ADSI que representa una entrada de propiedad.                    | [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Objeto ADSI que representa un valor de propiedad.                    | [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Objeto ADSI que representa un valor de propiedad.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Objeto ADSI que representa un descriptor de seguridad.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




