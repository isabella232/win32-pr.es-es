---
title: Enlace en tiempo de tarde de lo que sucede en el pasado
description: En este tema se describe cómo funciona el enlace en tiempo de tarde en ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, enlace en tiempo de tarde, lo que sucede en el centro
- enlace de AD, enlace en tiempo de tarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c479472a2974f31e8ecdd4308b01cf7c7251eada3f907d5d90ecf152028399b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637895"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Enlace en tiempo de tarde: ¿Qué está ocurriendo en primer lugar?

En la lista siguiente se describe el proceso general para realizar un enlace en tiempo de ejecución:

-   Algo se enlaza a un objeto de directorio ADSI. Por ejemplo, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" se enlaza mediante el enlace en tiempo de tarde COM. Esto hace que ADSI llame al [**método QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en la **interfaz IDispatch.**
-   ADSI busca un objeto en la clase de usuario y crea [](/windows/desktop/api/Iads/nn-iads-iads)un objeto que admite las interfaces adecuadas, como ID, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI realiza una búsqueda en el Registro y busca CLID de extensión para el usuario. Tenga en cuenta que ADSI almacena en caché estos datos.
-   Algo realiza una llamada al **método MyNewMethod.** ADSI busca su identificador de envío y los identificadores de envío para otras extensiones adsi. A continuación, ADSI busca la extensión que atiende esta llamada y llama a la [**interfaz IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para esa extensión.
-   La extensión ejecuta la función .
-   Ahora, el escritor de cliente invoca el **método YourNewMethod** mediante la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para la extensión actual. La implementación de **IDispatch** de la extensión vuelve a delegar en **IDispatch** para ADSI.
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para ADSI busca de nuevo la extensión adecuada o, a continuación, llama a la extensión adecuada mediante la interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para esa extensión.

 

 