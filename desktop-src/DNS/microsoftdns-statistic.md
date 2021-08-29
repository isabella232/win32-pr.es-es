---
title: MicrosoftDNS_Statistic clase
description: La clase MicrosoftDNS \_ Statistic representa una única estadística del servidor DNS.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic dns de clase
- MicrosoftDNS_Statistic clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a489f8a4d9e3d442d4157243594c187a799d20a1d07b3ccc68135e73ddce288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815665"
---
# <a name="microsoftdns_statistic-class"></a>Clase MicrosoftDNS \_ Statistic

La **clase MicrosoftDNS \_ Statistic** representa una única estadística del servidor DNS.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a>Miembros

La **clase MicrosoftDNS \_ Statistic** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ Statistic** tiene estas propiedades.

<dl> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Representación numérica de **CollectionName.**

</dd> <dt>

**CollectionName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la colección a la que pertenece la estadística.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el FQDN o la dirección IP del servidor DNS que contiene la estadística.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la estadística.

</dd> <dt>

**StringValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de cadena de la estadística, que solo se usa cuando el valor estadístico no se representa como DWORD.

</dd> <dt>

**Valor**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor numérico de la estadística, representado como DWORD.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MicrosoftDNS \_ StatisticCollection](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





