---
title: MicrosoftDNS_SOAType clase
description: Subclase de ResourceRecord de MicrosoftDNS que representa un registro de inicio de autoridad \_ (SOA).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- MicrosoftDNS_SOAType DNS de clase
- MicrosoftDNS_SOAType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2a9b0317c6e842558f771dcd10ec7707602e17510ffc20c3a9684fc94bf7d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163149"
---
# <a name="microsoftdns_soatype-class"></a>Clase SOAType de MicrosoftDNS \_

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de inicio de autoridad (SOA).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a>Miembros

La **clase \_ SOAType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ SOAType de MicrosoftDNS** tiene estos métodos.



| Método     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modificar** | Actualiza el TTL, el número de serie soa, el servidor principal, la entidad responsable, el intervalo de actualización, el retraso de reintento, el límite de expiración y el TTL mínimo (para la zona) a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ SOAType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**ExpireLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, antes de que una zona que no responde ya no sea autoritativa.

</dd> <dt>

**MinimumTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Límite inferior en el tiempo, en segundos, que un servidor DNS o un solucionador de almacenamiento en caché pueden almacenar en caché cualquier registro de recursos de la zona a la que pertenece este registro.

</dd> <dt>

**PrimaryServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Servidor DNS autoritativo para la zona a la que pertenece el registro.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, antes de que se actualice la zona que contiene este registro.

</dd> <dt>

**ResponsibleParty**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la parte responsable de la zona a la que pertenece el registro.

</dd> <dt>

**RetryDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, antes de reintentar una actualización con error de la zona a la que pertenece este registro.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de serie del registro SOA.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método Modify de la clase SOAType de MicrosoftDNS \_**](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





