---
description: Quita un equipo de un dominio o un grupo de trabajo.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Método UnjoinDomainOrWorkgroup de la clase Win32_ComputerSystem
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
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907466"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método UnjoinDomainOrWorkgroup de la clase de Win32 \_ ComputerSystem

El método **UnjoinDomainOrWorkgroup** quita un equipo de un dominio o un grupo de trabajo.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*Contraseña* \[ de de\]
</dt> <dd>

Si el parámetro *username* especifica un nombre de cuenta, el parámetro *password* debe apuntar a la contraseña que se va a usar al conectarse al controlador de dominio. De lo contrario, este parámetro debe ser **null**.

> [!Note]  
> La *contraseña* debe usar un nivel de autenticación alto, no menor que la **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, al conectarse a WinMgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en el puntero [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Si es local a WinMgmt, esto no es un problema.

 

</dd> <dt>

*Nombre de usuario* \[ de\]
</dt> <dd>

Puntero a una cadena de caracteres terminada en null que especifica el nombre de la cuenta que se va a usar al conectarse al controlador de dominio. Debe especificar un dominio y una cuenta de usuario, por ejemplo, "dominio \\ usuario" o " user@domain ". Si este parámetro es **null**, se utiliza el contexto del llamador.

> [!Note]  
> El *nombre de usuario* debe usar un nivel de autenticación alto, no menor que la **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, al conectarse a WinMgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en el puntero [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Si es local a WinMgmt, esto no es un problema.

 

</dd> <dt>

*FUnjoinOptions* \[ de\]
</dt> <dd>

Conjunto de marcadores de bits que definen las opciones de unjoin.

<dt>



  (0)


</dt> <dd>

Predeterminada. No hay opciones.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ \_Eliminación** de cuenta (4)


</dt> <dd>

Deshabilite la cuenta de Active Directory después de la operación de desunión, pero no elimine la cuenta.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método **UnjoinDomainOrWorkgroup** devuelve 0 (cero) si se realiza correctamente o no hay opciones implicadas. Cualquier otro valor indica un error. Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Después de llamar a este método, reinicie el equipo afectado para aplicar los cambios.

## <a name="examples"></a>Ejemplos

[Desasociar un equipo de un dominio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) El ejemplo de VBScript Desune el equipo local de su dominio actual y deshabilita la cuenta de equipo.

El ejemplo de [script separar un equipo de un dominio con VBS](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) quita la Unión de un equipo especificado de un dominio. .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ComputerSystem de Win32 \_**](win32-computersystem.md)
</dt> <dt>

[**Método JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

