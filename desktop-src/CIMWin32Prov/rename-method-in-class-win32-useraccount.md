---
description: Cambia el nombre de una cuenta de usuario.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Método Rename de la Win32_UserAccount clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062651"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Método Rename de la clase UserAccount de Win32 \_

El **método Cambiar nombre** de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) cambia el nombre de una cuenta de usuario.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nuevo nombre de cuenta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Correcto.

</dd> <dt>

**Instancia no encontrada**
</dt> <dd>

1

No se encontró la instancia.

</dd> <dt>

**Instancia necesaria**
</dt> <dd>

2

Instancia necesaria.

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

**Dominio no encontrado**
</dt> <dd>

5

Dominio no encontrado.

</dd> <dt>

**Solo se permite la operación en el controlador de dominio principal del dominio.**
</dt> <dd>

6

La operación solo se permite en el controlador de dominio principal del dominio.

</dd> <dt>

**No se permite la operación en la última cuenta administrativa.**
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

Otro error de API.

</dd> <dt>

**Error interno**
</dt> <dd>

10

Error interno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta funcionalidad se implementa como un método para proporcionar un contexto independiente para el nuevo nombre que se puede distinguir del valor de propiedad de clave de Nombre asociado a la instancia que se va a modificar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**UserAccount de Win32 \_**](win32-useraccount.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

