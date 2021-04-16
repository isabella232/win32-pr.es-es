---
description: Define el tipo de puntos de conexión que se pueden utilizar para conectarse a un servicio.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumeración UpdateEndpointType (UpdateEndpointAuth. h)
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
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540123"
---
# <a name="updateendpointtype-enumeration"></a>Enumeración UpdateEndpointType

Define el tipo de puntos de conexión que se pueden utilizar para conectarse a un servicio.

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

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

Un punto de conexión cliente-servidor que se utiliza para conectarse al servicio de actualización, como Windows Update, Microsoft Update y servidor WSUS en un entorno corporativo, para buscar información sobre las actualizaciones que pueden ser aplicables al equipo.

El servicio de actualización devuelve información sobre las actualizaciones publicadas, revisadas o retiradas desde la última vez que el cliente realizó una sincronización con el servidor.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

Un punto de conexión de informes que se utiliza cuando el cliente informa de los resultados de los análisis, las descargas y vuelve a instalarse en el servicio de actualización.

En el caso de los servicios públicos (Windows Update y Microsoft Update), esto se hace para la supervisión de la calidad.

En el caso de los servicios privados, como un servidor WSUS corporativo, el tipo de punto de conexión thhis también permite que el servidor recopile el inventario y otra información sobre los equipos cliente que se están controlando.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

Un punto de conexión de actualización automática que se utiliza cuando el equipo cliente se pone en contacto con un servicio de actualización para comprobar si hay una nueva versión del software cliente del agente de Windows Update.

El punto de conexión de actualización automática usa un protocolo diferente, el extremo de Client-Server para que se puedan distribuir las actualizaciones automáticas, incluso si hay una condición de error que podría impedir que la sincronización de cliente-servidor normal funcione en un equipo cliente determinado.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Un punto de conexión de Reglamento que se utiliza cuando el equipo cliente se pone en contacto con el servicio de Reglamento para actuar sobre una actualización determinada que es aplicable al equipo de destino.

El servicio de regulación puede indicar si la actualización está "regulada" (también conocida como "limitada"); en otras palabras, el servicio de regulación puede indicar al equipo cliente que no debe actuar en una actualización determinada, aunque esa actualización parezca ser aplicable.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

Un punto de conexión de destino simple que solo se usa con servicios privados (servidores WSUS en entornos corporativos). En un entorno corporativo, los equipos cliente se pueden asignar a grupos de destino concretos y las actualizaciones se pueden aprobar para su instalación en equipos en algunos grupos, pero no en otros.

Por ejemplo, el administrador de WSUS puede crear un grupo de "pruebas" para los equipos que se usan para probar nuevas actualizaciones, y el administrador puede aprobar las actualizaciones recién publicadas para instalarlas en los equipos del grupo de prueba sin que se aprueben para su instalación en otros equipos de la organización. El intercambio de destino sencillo se usa para permitir que un equipo cliente se registre en el servidor WSUS y permitir que el servidor indique al equipo cliente en qué grupo se encuentra.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Un punto de conexión de cliente-servidor protegido que permite a un cliente obtener información sobre las aplicaciones que necesitan licencias para que se puedan usar en un equipo cliente. Actualmente, Windows 8 solo usa este marco de licencias para implementar aplicaciones y actualizaciones que se obtienen a través de la tienda Windows. Windows Update, Microsoft Update o WSUS no usan actualmente el punto de conexión protegido-cliente-servidor.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

Un cliente usa el punto de conexión de autenticación de servicio secundario para proporcionar la autenticación antes de obtener información sobre las aplicaciones que necesitan licencias para que se puedan usar en un equipo cliente. Actualmente, Windows 8 solo emplea este marco de licencias para implementar aplicaciones y actualizaciones que se obtienen a través de la tienda Windows. Windows Update, Microsoft Update o WSUS no usan actualmente el punto de conexión de autenticación de servicio secundario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




