---
title: MicrosoftDNS_SRVType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro de servicio (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType dns de clase
- MicrosoftDNS_SRVType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaff2c570647386ecd8d53592b940cbd54477764b323b5457dbec3357cf3b98c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104015"
---
# <a name="microsoftdns_srvtype-class"></a>Clase SRVType de MicrosoftDNS \_

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de servicio (SRV).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a>Miembros

La **clase \_ SRVType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ SRVType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un tipo SRV de RR en función de los datos de los parámetros de entrada del método: nombre del servidor DNS del registro, nombre de contenedor, nombre de propietario/destino, clase (valor predeterminado = IN), valor de período de vida y prioridad, peso, puerto y nombre de dominio del host de destino. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Actualiza TTL, Priority, Weight, Port y Domain Name a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>                  |



 

### <a name="properties"></a>Propiedades

La **clase \_ SRVType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**Puerto**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puerto utilizado en el host de destino de un servicio de protocolo.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad del host de destino especificado en el nombre del propietario. Los números más bajos implican prioridades más altas.

</dd> <dt>

**SRVDomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN del host de destino. Un destino de \\ significa que el servicio no está disponible en este \\ dominio.

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Peso del host de destino. Esto resulta útil al seleccionar entre hosts que tienen la misma prioridad. Las posibilidades de usar este host deben ser proporcionales a su peso.

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

[**Método CreateInstanceFromPropertyData de la clase SRVType de MicrosoftDNS \_**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase SRVType de MicrosoftDNS \_**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





