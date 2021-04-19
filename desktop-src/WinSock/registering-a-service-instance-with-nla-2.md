---
description: Los clientes NLA pueden registrar información de configuración de red en todo el sistema, lo que permite que las consultas futuras devuelvan la información de configuración especificada independientemente de si la red está activa.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrar una instancia de servicio con NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696932"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrar una instancia de servicio con NLA

Los clientes NLA pueden registrar información de configuración de red en todo el sistema, lo que permite que las consultas futuras devuelvan la información de configuración especificada independientemente de si la red está activa. Esta funcionalidad permite que los clientes de NLA afecten a una experiencia de usuario de información de red coherente entre varias aplicaciones.

## <a name="parameters"></a>Parámetros

Para registrar una instancia de servicio con el proveedor de servicios de reconocimiento de ubicación de red, utilice la función [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) . Para registrar correctamente una instancia de servicio, ciertos parámetros de la función **WSASetService** se deben establecer con la información adecuada, como se explica en esta sección. Para una referencia rápida, la función **WSASetService** tiene la siguiente sintaxis:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Para el parámetro *lpqsRegInfo* , proporcione una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) desde el resultado de una consulta NLA SP o construya el cumplimiento de los requisitos de una consulta de SP NLA, como se especifica en [consultar NLA](querying-nla-2.md).

Las operaciones admitidas para el parámetro *essOperation* son las siguientes:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>registro de RNRSERVICE \_
</dt> <dd>

La red definida en la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionada en *lpqsRegInfo* se hace persistente para el usuario activo almacenando la instancia de red en el subárbol del registro para el usuario actual, lo que permite la suplantación.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ eliminar
</dt> <dd>

Si la red definida en la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionada en *lpqsRegInfo* es persistente, se quitará.

</dd> </dl>

La operación especificada en el parámetro *essOperation* se puede modificar con las siguientes opciones, que se pueden especificar con la lógica OR binaria:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nombre descriptivo de NLA \_
</dt> <dd>

Cuando se usa con \_ el registro RNRSERVICE, se comprueba la validez del campo *lpszComment* de la red definida en *lpqsRegInfo* y se almacena de forma persistente. Cuando se usa con RNRSERVICE \_ Delete y la red definida tiene un nombre descriptivo, se quita el nombre descriptivo pero la entrada de red se deja intacta.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_red de AllUsers de NLA \_
</dt> <dd>

Cuando se usa con \_ el registro RNRSERVICE, la entrada se almacena de forma persistente en HKEY \_ local \_ Machine, lo que lo pone a disposición durante las consultas a todos los usuarios en el equipo local. Cuando se usa con RNRSERVICE \_ Delete, la red especificada se quita de \_ la \_ máquina local HKEY. Se devuelve un error si la red especificada no está presente. Para eliminar una red del subárbol del registro del usuario actual, no se debe especificar esta marca. Esta marca solo es válida en el contexto de seguridad de un administrador del sistema local.

</dd> </dl>

NLA admite los siguientes códigos de error para las llamadas a la función [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :

| Error             | Significado                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA.                                                                  |
| WSAEACCESS        | \_La red AllUsers de NLA \_ se especificó en *dwControlFlags* mientras no se encontraba en el contexto de seguridad de un administrador del sistema local.                                                |
| WSAEALREADY       | La red especificada ya está almacenada de forma persistente en la manera solicitada y no se ha especificado ninguna marca en *dwControlFlags* para indicar una actualización de la entrada existente. |
| WSAEAFNOSUPPORT   | Se especificó una familia de protocolos para la que no se admite. Solo se admiten familias de protocolo IP en NLA.                                                             |
| WSAEPFNOSUPPORT   | Se especificó un protocolo para el que no se admite. Solo se admite el protocolo IP en NLA.                                                                              |



 

 

 



