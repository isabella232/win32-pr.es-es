---
title: Win32_SessionBrokerFarmAccount (clase)
description: La \_ clase Win32 SessionBrokerFarmAccount ya no está disponible para su uso a partir de Windows Server 2012. | Win32_SessionBrokerFarmAccount (clase)
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerFarmAccount de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820823"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>\_Clase Win32 SessionBrokerFarmAccount

\[La clase **Win32 \_ SessionBrokerFarmAccount** ya no está disponible para su uso a partir de Windows Server 2012.\]

Define una cuenta de granja de agentes de sesiones.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionBrokerFarmAccount de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ SessionBrokerFarmAccount** tiene estos métodos.



| Método                                                      | Descripción                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | Elimina la cuenta de la granja.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ SessionBrokerFarmAccount de Win32** tiene estas propiedades.

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre del dominio al que pertenece la cuenta de la granja de servidores.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El nombre de la cuenta de la granja.

</dd> <dt>

**AccountPassword**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La contraseña de la cuenta de la granja.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Primer nombre de entidad de seguridad de servicio (SPN) asociado a la cuenta de la granja.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El segundo SPN asociado a la cuenta de la granja.

</dd> <dt>

**ComputerDNSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre DNS del equipo asociado a la cuenta de la granja.

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

El nombre de la granja de agentes de sesiones.

</dd> <dt>

**Manual**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si la contraseña de la cuenta se ha actualizado manualmente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                              |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

