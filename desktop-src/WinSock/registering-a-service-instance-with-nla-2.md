---
description: Los clientes NLA pueden registrar información de configuración de red en todo el sistema, lo que permite que las consultas futuras devuelvan la información de configuración especificada independientemente de si la red está activa.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registro de una instancia de servicio con NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623f28d30d02cd3a1266e173dbe28270f377a55c3f59f8ff095cf3d023a80eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641685"
---
# <a name="registering-a-service-instance-with-nla"></a>Registro de una instancia de servicio con NLA

Los clientes NLA pueden registrar información de configuración de red en todo el sistema, lo que permite que las consultas futuras devuelvan la información de configuración especificada independientemente de si la red está activa. Esta funcionalidad permite a los clientes de NLA afectar a una experiencia de usuario coherente con la información de red en varias aplicaciones.

## <a name="parameters"></a>Parámetros

Para registrar una instancia de servicio con el proveedor de Servicios de reconocimiento de ubicación de red, use la [**función WSASetService.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) Para registrar correctamente una instancia de servicio, determinados parámetros de la función **WSASetService** deben establecerse con la información adecuada, como se explica en esta sección. Como referencia rápida, la **función WSASetService** tiene la sintaxis siguiente:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Para el parámetro *lpqsRegInfo,* proporcione una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) a partir de un resultado de consulta de NLA SP o construido conforme a los requisitos de una consulta de NLA SP, como se especifica en Consulta [de NLA](querying-nla-2.md).

Las operaciones admitidas para *el parámetro essOperation* son las siguientes:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>REGISTRO DE \_ RNRSERVICE
</dt> <dd>

La red definida en la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionada en *lpqsRegInfo* se hace persistente para el usuario activo almacenando la instancia de red en el subárbol del Registro para el usuario actual, lo que permite la suplantación.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ DELETE
</dt> <dd>

Si la red definida en la [**estructura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionada en *lpqsRegInfo* es persistente, se quitará.

</dd> </dl>

La operación especificada en el parámetro *essOperation* se puede modificar mediante las siguientes opciones, que se pueden especificar con lógica OR binaria:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NOMBRE DESCRIPTIVO DE NLA \_ \_
</dt> <dd>

Cuando se usa con RNRSERVICE REGISTER, se comprueba la validez del campo lpszComment de la red definida en \_ *lpqsRegInfo* y se almacena de forma persistente.  Cuando se usa con RNRSERVICE DELETE y la red definida tiene un nombre descriptivo, se quita el nombre descriptivo, pero la entrada de red \_ se deja intacta.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>RED NLA \_ ALLUSERS \_
</dt> <dd>

Cuando se usa con RNRSERVICE REGISTER, la entrada se almacena de forma persistente en HKEY LOCAL MACHINE, lo que la hace disponible durante las consultas a todos los usuarios \_ \_ del equipo \_ local. Cuando se usa con RNRSERVICE \_ DELETE, la red especificada se quita de HKEY \_ LOCAL \_ MACHINE. Se devuelve un error si la red especificada no está presente. Para eliminar una red del subárbol del Registro del usuario actual, no se debe especificar esta marca. Esta marca solo es válida en el contexto de seguridad de un administrador del sistema local.

</dd> </dl>

NLA admite los siguientes códigos de error para [**las llamadas de función WSASetService:**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

| Error             | Significado                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA.                                                                  |
| WSAEACCESS        | NLA \_ ALLUSERS \_ NETWORK se especificó en *dwControlFlags,* pero no en el contexto de seguridad de un administrador del sistema local.                                                |
| WSAEALREADY       | La red especificada ya se almacena de forma persistente de la manera solicitada y no se especificó ninguna marca en *dwControlFlags* para indicar una actualización de la entrada existente. |
| WSAEAFNOSUPPORT   | Se especificó una familia de protocolos para la que no hay compatibilidad. Solo se admiten familias de protocolos IP en NLA.                                                             |
| WSAEPFNOSUPPORT   | Se especificó un protocolo para el que no hay compatibilidad. Solo se admite el protocolo IP en NLA.                                                                              |



 

 

 



