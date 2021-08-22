---
description: Recupera los certificados del sistema en un sistema host.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Método GetSystemCertificates de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bdc3fe1e2a12809dceb14a23e087d3e844f5e1a51401171b68dfe41303739c2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253625"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a>Método GetSystemCertificates de la clase ReplicationService de Msvm \_

Recupera los certificados del sistema en un sistema host.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodedCertificates* \[ out\]
</dt> <dd>

Si se realiza correctamente, recibe los certificados disponibles desde el almacén personal de la máquina local. Cada entrada es una cadena de certificado codificada en base 64. Esta cadena se puede convertir en una matriz de bytes mediante la construcción de un objeto X509Certificate2.

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

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está** disponible (32777)
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

 

 




