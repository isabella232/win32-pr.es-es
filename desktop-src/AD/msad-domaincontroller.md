---
title: MSAD_DomainController clase
description: Representa el controlador de dominio (DC) en el que se ejecuta el proveedor WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController clase Active Directory
- MSAD_DomainController clase Active Directory , descrita
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
ms.openlocfilehash: a428d1c852d93fb34bfc3188219bd8ffdc5020ae65c5f9191c44d075b603a143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186090"
---
# <a name="msad_domaincontroller-class"></a>Clase DomainController de MSAD \_

Representa el controlador de dominio (DC) en el que se ejecuta el proveedor WMI.

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

La **clase \_ DomainController de MSAD** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ DomainController de MSAD** tiene estos métodos.



| Método                                                 | Descripción                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Invoca a Knowledge Consistency Checker para comprobar la topología de replicación.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ DomainController de MSAD** tiene estas propiedades.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre común del objeto de servidor.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X.500 del [**objeto NTDS-DSA.**](/windows/desktop/ADSchema/c-ntdsdsa)

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el servicio de localizador del controlador de dominio se anuncia correctamente. **TRUE** si el servicio de localizador del controlador de dominio se anuncia correctamente; de lo contrario, **FALSE**.

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el controlador de dominio es un servidor de catálogo global. **TRUE** si el controlador de dominio es un servidor de catálogo global; de lo contrario, **FALSE**.

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el controlador de dominio ha obtenido otro grupo de RID. **TRUE** si el controlador de dominio ha obtenido otro grupo de RID y la asignación de RID en este controlador de dominio puede continuar incluso si se agota el grupo actual de RID; de lo contrario, **FALSE**.

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si el controlador de dominio está registrado correctamente en DNS. **TRUE** si el controlador de dominio está registrado correctamente en DNS; de lo contrario, **FALSE**.

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si SysVol se ha publicado correctamente. **TRUE** si SysVol se ha publicado correctamente; de lo contrario, **FALSE**.

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el GUID asociado al objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) en el contenedor de configuración. El **objeto NTDS-DSA** representa el Dominio de Active Directory DSA del servicio en el servidor.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el porcentaje de RID que quedan en el grupo de RID actual en este controlador de dominio.

</dd> <dt>

**SiteName**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el sitio en el que existe el controlador de dominio.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de adición de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de eliminación de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de modificación de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de sincronización de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo de la operación de actualización de replicación más antigua que todavía está en la cola de este controlador de dominio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

