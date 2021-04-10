---
description: Cambia el nombre de un nombre de cuenta de usuario.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153369"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Cambiar el nombre del método de la \_ clase Win32 cuentadeusuario

El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cambia el nombre de un nombre de cuenta de usuario.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Nuevo nombre de cuenta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Correcto.

</dd> <dt>

**No se encontró la instancia**
</dt> <dd>

1

No se encuentra la instancia.

</dd> <dt>

**Instancia requerida**
</dt> <dd>

2

Instancia requerida.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

3

Parámetro no válido.

</dd> <dt>

**Usuario no encontrado**
</dt> <dd>

4

Usuario no encontrado.

</dd> <dt>

**No se encontró el dominio**
</dt> <dd>

5

No se encontró el dominio.

</dd> <dt>

**La operación solo se permite en el controlador de dominio principal del dominio**
</dt> <dd>

6

La operación solo se permite en el controlador de dominio principal del dominio.

</dd> <dt>

**La operación no se permite en la última cuenta administrativa.**
</dt> <dd>

7

</dd> <dt>

**No se permite la operación en grupos especiales especificados; usuario, administrador, local o invitado.**
</dt> <dd>

8

No se permite la operación en grupos especiales especificados: usuario, administrador, local o invitado.

</dd> <dt>

**Otro error de API**
</dt> <dd>

9

Otro error de la API.

</dd> <dt>

**Error interno**
</dt> <dd>

10

Error interno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta funcionalidad se implementa como un método para proporcionar un contexto independiente para el nuevo nombre que se puede distinguir del valor de la propiedad clave para el nombre que está asociado a la instancia que se va a modificar.

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

[**Cuentadeusuario de Win32 \_**](win32-useraccount.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

