---
description: Quita un sistema informático de un dominio o grupo de trabajo.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Método UnjoinDomainOrWorkgroup de la Win32_ComputerSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992aa6c84f912f705e02252d1ac6d24422934edb991c049de188ab5fb0ccbfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105075"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método UnjoinDomainOrWorkgroup de la clase ComputerSystem de Win32 \_

El **método UnjoinDomainOrWorkgroup** quita un sistema informático de un dominio o grupo de trabajo.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Contraseña* \[ En\]
</dt> <dd>

Si el *parámetro UserName* especifica un nombre de cuenta, el parámetro *Password* debe apuntar a la contraseña que se usará al conectarse al controlador de dominio. De lo contrario, este parámetro debe ser **NULL.**

> [!Note]  
> *La* contraseña debe usar un nivel de autenticación alto, no menor que **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**, al conectarse a Winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en el puntero [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Si es local en Winmgmt, esto no es un problema.

 

</dd> <dt>

*UserName* \[ En\]
</dt> <dd>

Puntero a una cadena de caracteres terminada en null constante que especifica el nombre de cuenta que se usará al conectarse al controlador de dominio. Debe especificar un dominio y una cuenta de usuario, por ejemplo, "usuario \\ de dominio" o user@domain "." Si este parámetro es **NULL,** se usa el contexto del autor de la llamada.

> [!Note]  
> *UserName* debe usar un nivel de autenticación alto, no menor que **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**, al conectarse a Winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en el puntero [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Si es local en Winmgmt, esto no es un problema.

 

</dd> <dt>

*FUnjoinOptions* \[ En\]
</dt> <dd>

Conjunto de marcas de bits que definen las opciones de unirse.

<dt>



  (0)


</dt> <dd>

Predeterminada. No hay opciones.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ ACCT \_ DELETE** (4)


</dt> <dd>

Deshabilite Active Directory cuenta después de la operación de desenlace, pero no elimine la cuenta.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El **método UnjoinDomainOrWorkgroup** devuelve 0 (cero) si se ejecuta correctamente o cuando no hay ninguna opción implicada. Cualquier otro valor indica un error. Para obtener códigos de error, [**vea Constantes de error wmi**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Después de llamar a este método, reinicie el equipo afectado para aplicar los cambios.

## <a name="examples"></a>Ejemplos

[Unirse a un equipo desde un dominio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) El ejemplo de VBScript une el equipo local de su dominio actual y deshabilita la cuenta de equipo.

El [ejemplo de script Unjoin a Computer from a Domain using VBS (Unjoin a Computer from a Domain using VBS)](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) unjoins a specified computer from a domain (Unjoin a Computer from a Domain using VBS script sample unjoins a specified computer from a domain). .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Equipo \_ Win32System**](win32-computersystem.md)
</dt> <dt>

[**Método JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

