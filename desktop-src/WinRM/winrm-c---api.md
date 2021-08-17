---
title: WinRM C++ API
description: Las Windows de administración remota se pueden usar para obtener datos o administrar recursos en un equipo remoto. Esta API está pensada principalmente para uso interno. Se recomienda usar la API de Shell de cliente de WinRM siempre que sea posible.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742951"
---
# <a name="winrm-c-api"></a>WinRM C++ API

Las Windows de administración remota se pueden usar para obtener datos o administrar [*recursos*](windows-remote-management-glossary.md) en un equipo remoto. Esta API está pensada principalmente para uso interno. Se recomienda usar la API de Shell de cliente [de WinRM siempre](client-shell-api.md) que sea posible. Las interfaces se corresponden estrechamente con [la API de scripting de WinRM.](winrm-scripting-api.md)

Las interfaces winRM que heredan directamente de **IDispatch** tienen un objeto de scripting correspondiente. Para obtener más información, vea [WinRM Scripting API](winrm-scripting-api.md).

En el caso de las aplicaciones multiproceso, WinRM no admite subprocesos independientes que accedan al mismo [**objeto IWSMAN.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)

WinRM proporciona las interfaces siguientes.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Proporciona métodos y propiedades que se usan para crear una nueva sesión y administrar una sesión establecida. [**WSMan es**](wsman.md) el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Proporciona métodos y propiedades que se usan para crear un [**nuevo objeto IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) Este método está disponible para el objeto de scripting [**de WSMan.**](wsman.md)

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Define el nombre de usuario y la contraseña usados para las conexiones remotas. [**ConnectionOptions es**](connectionoptions.md) el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Define las operaciones de red y las propiedades disponibles para la sesión. [**Session**](session.md) es el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Representa una colección de resultados devueltos por la enumeración de un recurso. [**El enumerador**](enumerator.md) es el objeto de scripting correspondiente.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Proporciona la ruta de acceso a un recurso. Puede usar un objeto [**IWSManResourceLocator en**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) lugar de un [*URI de*](windows-remote-management-glossary.md) recurso en operaciones de objeto [**de**](session.md) sesión. [**ResourceLocator es**](resourcelocator.md) el objeto de scripting correspondiente.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> </dl>

 

 




