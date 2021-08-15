---
title: Mensajes de error extendidos de ADSI
description: Este tema contiene una lista de temas que explican cómo trabajar con mensajes de error ADSI devueltos por IADs, IADsContainer, IDirectoryObject e IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Mensajes de error extendidos de ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2bf4c7faef20feeb868fdcbb0e36d7f1ad5d0b9c68cc8879d5019e81e186a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180879"
---
# <a name="adsi-extended-error-messages"></a>Mensajes de error extendidos de ADSI

Además de los **valores HRESULT,** varios proveedores de sistemas ADSI (principalmente LDAP) devuelven datos de error adicionales para las operaciones realizadas por las interfaces siguientes:

-   [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Una parte de estos datos de error extendidos es la cadena enviada por el servidor como parte del resultado del mensaje.

Llame [**a ADsGetLastError para**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) recuperar estos mensajes de error extendidos. El primer parámetro de esta función, *lpError*, es un **valor DWORD.** Para un servidor Active Directory, ADSI intenta asignar un mensaje de error LDAP a un código de error de Win32 adecuado y asigna el valor de código de error de Win32 a *lpError*. Al no resolver la asignación, ADSI asigna **ERROR \_ INVALID \_ DATA** a *lpError*, como ocurre con cualquier otro servidor de directorios. En todos los casos, ADSI retransmite la cadena de la descripción del error del servidor al cliente a través de *lpErrorBuf*, el segundo parámetro de la función **ADsGetLastError.**

 

 




