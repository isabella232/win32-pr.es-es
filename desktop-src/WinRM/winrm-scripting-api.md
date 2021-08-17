---
title: WinRM Scripting API
description: Windows Los objetos de scripting de administración remota se implementan como una capa por encima del WS-Management protocolo.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742763"
---
# <a name="winrm-scripting-api"></a>WinRM Scripting API

Windows Los objetos de scripting de administración remota se implementan como una capa por encima del [protocolo WS-Management](ws-management-protocol.md). Los objetos de scripting permiten obtener datos o administrar [*recursos*](windows-remote-management-glossary.md) en equipos locales y remotos.

## <a name="ws-management-objects"></a>WS-Management objetos

Cada objeto de scripting tiene una interfaz de C++ correspondiente. Para obtener más información, vea [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).

La API de scripting de WinRM proporciona los siguientes objetos.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Define el nombre de usuario y la contraseña usados para las conexiones remotas. El nombre de usuario y la contraseña se pasan al llamar al [**método CreateConnectionOptions.**](wsman-createconnectionoptions.md) Para obtener más información, [vea Obtener datos de un equipo remoto.](obtaining-data-from-a-remote-computer.md) La interfaz de C++ correspondiente [**es IWSManConnectionOptions.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerador**](enumerator.md)
</dt> <dd>

Representa una colección de resultados devueltos al enumerar un recurso. Para obtener más información, [vea Enumerar o enumerar todas las instancias de un recurso.](enumerating-or-listing-all-instances-of-a-resource.md) La interfaz de C++ correspondiente es [**IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Proporciona la ruta de acceso a un recurso. Puede usar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de un [*URI*](windows-remote-management-glossary.md) de recurso en operaciones de objeto [**session,**](session.md) como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md) La interfaz de C++ correspondiente es [**IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sesión**](session.md)
</dt> <dd>

Define las operaciones de red y las propiedades disponibles para la sesión, [**como Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md). Para obtener más información, [vea Obtener datos del equipo local.](obtaining-data-from-the-local-computer.md) La interfaz de C++ correspondiente es [**IWSManSession.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

Proporciona métodos y propiedades que se usan para crear una nueva sesión o administrar una sesión establecida. Para obtener más información, vea [Using Windows Remote Management](using-windows-remote-management.md). Las interfaces de C++ correspondientes [**son IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) [**e IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Scripting en la Windows remota](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> </dl>

 

 




