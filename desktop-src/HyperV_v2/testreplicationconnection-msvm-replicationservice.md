---
description: Comprueba si la replicación se puede habilitar desde el sistema host actual al sistema de recuperación especificado.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Método TestReplicationConnection de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666309"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Método TestReplicationConnection de la \_ clase ReplicationService de MSVM

Comprueba si la replicación se puede habilitar desde el sistema host actual al sistema de recuperación especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RecoveryConnectionPoint* \[ de\]
</dt> <dd>

Nombre del punto de conexión. Para un clúster de recuperación, este es el nombre de la CAP de agente. Para un servidor de recuperación independiente, es el nombre del sistema host.

</dd> <dt>

*RecoveryServerPortNumber* \[ de\]
</dt> <dd>

Número de puerto del punto de conexión de recuperación.

</dd> <dt>

*AuthenticationType* \[ de\]
</dt> <dd>

El esquema de autenticación de recuperación. Debe ser uno de los valores siguientes.

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Autenticación integrada** (1)


</dt> <dd>

Autenticación Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticación basada en certificados** (2)


</dt> <dd>

Autenticación basada en certificados.

</dd> </dl> </dd> <dt>

*CertificateThumbPrint* \[ de\]
</dt> <dd>

Huella digital del certificado que se usará cuando el parámetro *AuthenticationType* sea autenticación basada en certificados.

</dd> <dt>

*BypassProxyServer* \[ de\]
</dt> <dd>

Omitir el servidor proxy al conectarse al servidor réplica.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

