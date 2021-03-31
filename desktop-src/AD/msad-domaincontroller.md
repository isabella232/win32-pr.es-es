---
title: MSAD_DomainController (clase)
description: Representa el controlador de dominio (DC) en el que se está ejecutando el proveedor WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController clase Active Directory
- Active Directory de MSAD_DomainController de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490739"
---
# <a name="msad_domaincontroller-class"></a>MSAD \_ DomainController (clase)

Representa el controlador de dominio (DC) en el que se está ejecutando el proveedor WMI.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>Miembros

La clase **MSAD \_ DomainController** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSAD \_ DomainController** tiene estos métodos.



| Método                                                 | Descripción                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Invoca el comprobador de coherencia de la información para comprobar la topología de replicación.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **MSAD \_ DomainController** tiene estas propiedades.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre común del objeto de servidor.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X. 500 del objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el servicio de localizador del controlador de dominio se está anunciando correctamente. **True** si el servicio de ubicación en el controlador de dominio se está anunciando correctamente; en caso contrario, **false**.

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el controlador de dominio es un servidor de catálogo global. **True** si el controlador de dominio es un servidor de catálogo global; en caso contrario, **false**.

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el controlador de dominio ha obtenido otro grupo de RID. **True** si el controlador de dominio ha obtenido otro grupo de RID y la asignación de los RID en este controlador de dominio puede continuar incluso si se ha agotado el grupo actual de RID; en caso contrario, **false**.

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el controlador de dominio está registrado correctamente en DNS. **True** si el controlador de dominio está registrado correctamente en DNS; en caso contrario, **false**.

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si SysVol se ha publicado correctamente. **True** si SYSVOL se ha publicado correctamente; en caso contrario, **false**.

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el GUID asociado al objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) en el contenedor de configuración. El objeto **NTDS-DSA** representa el proceso DSA de servicio dominio de Active Directory en el servidor.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el porcentaje de los RID que se dejan en el grupo de RID actual de este controlador de dominio.

</dd> <dt>

**Nombresitio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el sitio en el que existe el controlador de dominio.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de adición de replicación más antigua que aún está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de eliminación de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de modificación de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de sincronización de replicación más antigua que aún está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de actualización de replicación más antigua que aún está en la cola de este controlador de dominio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

