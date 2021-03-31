---
title: Mensajes de error extendidos de ADSI
description: Este tema contiene una lista de temas que explican cómo trabajar con mensajes de error ADSI devueltos por IADs, IADsContainer, IDirectoryObject y IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Mensajes de error extendidos de ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075089"
---
# <a name="adsi-extended-error-messages"></a>Mensajes de error extendidos de ADSI

Además de los valores **HRESULT** , varios proveedores de sistema ADSI (principalmente LDAP) devuelven datos de error adicionales para las operaciones realizadas por las siguientes interfaces:

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Una parte de estos datos de error extendidos es la cadena enviada por el servidor como parte del resultado del mensaje.

Llame a [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) para recuperar los mensajes de error extendidos. El primer parámetro de esta función, *lpError*, es un valor **DWORD** . Para un servidor de Active Directory, ADSI intenta asignar un mensaje de error LDAP a un código de error de Win32 adecuado y asigna el valor del código de error de Win32 a *lpError*. Si no se resuelve la asignación, ADSI asigna un **error de \_ \_ datos no válidos** a *lpError*, como lo hace para cualquier otro servidor de directorio. En todos los casos, ADSI retransmite fielmente la cadena de la descripción del error del servidor al cliente a través de *lpErrorBuf*, el segundo parámetro de la función **ADsGetLastError** .

 

 




