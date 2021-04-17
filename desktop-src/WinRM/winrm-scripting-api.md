---
title: API de scripting de WinRM
description: Administración remota de Windows objetos de scripting se implementan como una capa por encima del Protocolo de WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704733"
---
# <a name="winrm-scripting-api"></a>API de scripting de WinRM

Administración remota de Windows objetos de scripting se implementan como una capa por encima de la [protocolo WS-Management](ws-management-protocol.md). Los objetos de scripting le permiten obtener datos o administrar [*recursos*](windows-remote-management-glossary.md) en equipos locales y remotos.

## <a name="ws-management-objects"></a>Objetos WS-Management

Cada objeto de scripting tiene una interfaz de C++ correspondiente. Para obtener más información, vea [API](winrm-c---api.md) y [scripting de C++ de WinRM en administración remota de Windows](scripting-in-windows-remote-management.md).

La API de scripting de WinRM proporciona los siguientes objetos.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Define el nombre de usuario y la contraseña usados para las conexiones remotas. El nombre de usuario y la contraseña se pasan cuando se llama al método [**CreateConnectionOptions**](wsman-createconnectionoptions.md) . Para obtener más información, consulte [obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md). La interfaz de C++ correspondiente es [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Avanzó**](enumerator.md)
</dt> <dd>

Representa una colección de resultados devueltos al enumerar un recurso. Para obtener más información, consulte [enumeración o enumeración de todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md). La interfaz de C++ correspondiente es [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Proporciona la ruta de acceso a un recurso. Puede usar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de un [*URI de recurso*](windows-remote-management-glossary.md) en operaciones de objetos de [**sesión**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md). La interfaz de C++ correspondiente es [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sesión**](session.md)
</dt> <dd>

Define las operaciones de red y las propiedades disponibles para la sesión, como [**Session. Get**](session-get.md), [**Session. Enumerate**](session-enumerate.md), [**Session. Invoke**](session-invoke.md). Para obtener más información, consulte [obtener datos del equipo local](obtaining-data-from-the-local-computer.md). La interfaz de C++ correspondiente es [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

Proporciona métodos y propiedades que se usan para crear una nueva sesión o administrar una sesión establecida. Para obtener más información, vea [uso de administración remota de Windows](using-windows-remote-management.md). Las interfaces de C++ correspondientes son [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) y [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




