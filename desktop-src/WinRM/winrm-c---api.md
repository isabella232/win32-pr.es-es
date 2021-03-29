---
title: API de C++ para WinRM
description: Las interfaces de Administración remota de Windows se pueden usar para obtener datos o administrar recursos en un equipo remoto. Esta API está pensada principalmente para uso interno. En su lugar, se recomienda usar la API del shell de cliente de WinRM, siempre que sea posible.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994386"
---
# <a name="winrm-c-api"></a>API de C++ para WinRM

Las interfaces de Administración remota de Windows se pueden usar para obtener datos o administrar [*recursos*](windows-remote-management-glossary.md) en un equipo remoto. Esta API está pensada principalmente para uso interno. En su lugar, se recomienda usar la [API del shell de cliente de WinRM](client-shell-api.md) , siempre que sea posible. Las interfaces corresponden estrechamente a la [API de scripting de WinRM](winrm-scripting-api.md).

Las interfaces de WinRM que heredan directamente de **IDispatch** tienen un objeto de scripting correspondiente. Para obtener más información, consulte la [API de scripting de WinRM](winrm-scripting-api.md).

En el caso de las aplicaciones multiproceso, WinRM no es compatible con subprocesos independientes que acceden al mismo objeto [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .

WinRM proporciona las siguientes interfaces.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Proporciona métodos y propiedades que se usan para crear una nueva sesión y administrar una sesión establecida. [**WSMan**](wsman.md) es el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Proporciona métodos y propiedades que se usan para crear un nuevo [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator). Este método está disponible para el objeto de scripting [**WSMan**](wsman.md) .

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Define el nombre de usuario y la contraseña usados para las conexiones remotas. [**ConnectionOptions**](connectionoptions.md) es el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Define las operaciones de red y las propiedades disponibles para la sesión. La [**sesión**](session.md) es el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Representa una colección de resultados devueltos al enumerar un recurso. El [**enumerador**](enumerator.md) es el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Proporciona la ruta de acceso a un recurso. Puede usar un objeto [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) en lugar de un [*URI de recurso*](windows-remote-management-glossary.md) en operaciones de objeto de [**sesión**](session.md) . [**ResourceLocator**](resourcelocator.md) es el objeto de scripting correspondiente.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




