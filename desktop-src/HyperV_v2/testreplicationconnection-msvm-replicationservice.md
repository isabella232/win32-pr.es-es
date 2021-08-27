---
description: Comprueba si la replicación se puede habilitar desde el sistema host actual al sistema de recuperación especificado.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Método TestReplicationConnection de la Msvm_ReplicationService clase
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
ms.openlocfilehash: 729412ea2b506aedf09bcc77385c4c8b22d560d8cd8e6fc88b12c059c0bf049c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050385"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Método TestReplicationConnection de la clase ReplicationService de Msvm \_

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

*RecoveryConnectionPoint* \[ En\]
</dt> <dd>

Nombre del punto de conexión. Para un clúster de recuperación, este es el nombre cap del agente. Para un servidor de recuperación independiente, este es el nombre del sistema host.

</dd> <dt>

*RecoveryServerPortNumber* \[ En\]
</dt> <dd>

Número de puerto del punto de conexión de recuperación.

</dd> <dt>

*AuthenticationType* \[ En\]
</dt> <dd>

Esquema de autenticación de recuperación. Debe ser uno de los siguientes valores.

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

*CertificateThumbPrint* \[ En\]
</dt> <dd>

Huella digital del certificado que se va a usar *cuando el parámetro AuthenticationType* es la autenticación basada en certificados.

</dd> <dt>

*BypassProxyServer* \[ En\]
</dt> <dd>

Omita el servidor proxy al conectarse al servidor de réplica.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> </dl>

 

