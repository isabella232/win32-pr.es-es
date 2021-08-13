---
description: Define el tipo de puntos de conexión que se pueden usar para conectarse a un servicio.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumeración UpdateEndpointType (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 7fbfd67b3009fbe904284ea7a92cdea996d0a6e23a43a17639eb567d66536917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462915"
---
# <a name="updateendpointtype-enumeration"></a>Enumeración UpdateEndpointType

Define el tipo de puntos de conexión que se pueden usar para conectarse a un servicio.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**clientServer**
</dt> <dd>

Un punto de conexión cliente-servidor que se usa para conectarse al servicio de actualización, como Windows Update, Microsoft Update y el servidor WSUS en un entorno corporativo, para buscar información sobre las actualizaciones que pueden ser aplicables al equipo.

El servicio de actualización devuelve información sobre las actualizaciones publicadas, revisadas o retiradas desde la última vez que el cliente realizó una sincronización con el servidor.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**reporting**
</dt> <dd>

Un punto de conexión de informes que se usa cuando el cliente informa de los resultados de exámenes, descargas e instala de nuevo en el servicio de actualización.

En el caso de los servicios públicos (Windows Update y Microsoft Update), esto se realiza con fines de supervisión de calidad.

En el caso de los servicios privados, como un servidor WSUS corporativo, el tipo de punto de conexión también permite que el servidor recopile el inventario y otra información sobre los equipos cliente bajo administración.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**wuWuaSelfUpdate**
</dt> <dd>

Un punto de conexión de actualización automática que se usa cuando el equipo cliente se pone en contacto con un servicio de actualización para ver si hay una nueva versión del software cliente Windows Update Agent.

El punto de conexión de actualización automática usa un protocolo diferente y, a continuación, el punto de conexión de Client-Server para que las actualizaciones automáticas se puedan distribuir incluso si hay una condición de error que podría impedir que la sincronización cliente-servidor normal funcione en un equipo cliente determinado.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**vocación**
</dt> <dd>

Un punto de conexión de reglamento que se usa cuando el equipo cliente se pone en contacto con el servicio de regulación para actuar en una actualización determinada que se aplica al equipo de destino.

El servicio de regulación puede indicar si la actualización está "regulado" (también conocido como "limitada"), es decir, el servicio de regulación puede indicar al equipo cliente que no debe actuar en una actualización determinada, aunque parezca aplicable.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**simpleTargeting**
</dt> <dd>

Un punto de conexión de destino simple que solo se usa con servicios privados (servidores WSUS en entornos corporativos). En un entorno corporativo, los equipos cliente se pueden asignar a grupos de destino concretos y las actualizaciones se pueden aprobar para la instalación en equipos de algunos grupos, pero no en otros.

Por ejemplo, el administrador de WSUS puede crear un grupo de "Pruebas" para equipos que se usan para probar nuevas actualizaciones y el administrador puede aprobar actualizaciones recién publicadas para la instalación en equipos del grupo Pruebas sin aprobarlas para su instalación en otros equipos de la organización. El intercambio de destino simple se usa para permitir que un equipo cliente se registre en el servidor WSUS y para permitir que el servidor le informe al equipo cliente en qué grupo se encuentra.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**segurodClientServer**
</dt> <dd>

Un punto de conexión de cliente-servidor protegido que permite a un cliente obtener información sobre las aplicaciones que necesitan licencias para que se puedan usar en un equipo cliente. Actualmente, este marco de licencias solo se usa Windows 8 para implementar aplicaciones y actualizaciones que se obtienen a través de Windows Store. El punto de conexión secured-client-server no se usa actualmente en Windows Update, Microsoft Update o WSUS.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**secSecondaryServiceAuth**
</dt> <dd>

Un cliente usa el punto de conexión de autenticación de servicio secundario para proporcionar autenticación antes de obtener información sobre las aplicaciones que necesitan licencias para que se puedan usar en un equipo cliente. Actualmente, este marco de licencias solo lo usan Windows 8 implementar aplicaciones y actualizaciones que se obtienen a través de Windows Store. El punto de conexión de autenticación de servicio secundario no se usa actualmente en Windows Update, Microsoft Update o WSUS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                              |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



 

 




