---
description: Permite cambiar el nombre del grupo.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659325"
---
# <a name="rename-method-of-the-win32_group-class"></a>Cambiar el nombre del método de la clase de grupo de Win32 \_

El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) permite cambiar el nombre del grupo.

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

Nombre de la cuenta de usuario de Windows en el dominio especificado por la propiedad de **dominio** de esta clase.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método **Rename** puede devolver los códigos de error que se muestran en la lista siguiente. En el caso de valores enteros distintos de los enumerados, consulte los [ \_ códigos de retorno de WMI](/windows/desktop/WmiSdk/wmi-return-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Correcto.

</dd> <dt>

**No se encontró la instancia**
</dt> <dd>

1

</dd> <dt>

**Instancia requerida**
</dt> <dd>

2

</dd> <dt>

**parámetro no válido**
</dt> <dd>

3

</dd> <dt>

**Grupo no encontrado**
</dt> <dd>

4

</dd> <dt>

**No se encontró el dominio**
</dt> <dd>

5

</dd> <dt>

**La operación solo se permite en el controlador de dominio principal del dominio**
</dt> <dd>

6

</dd> <dt>

**No se permite la operación en grupos especiales especificados; usuario, administrador, local o invitado.**
</dt> <dd>

7

</dd> <dt>

**Otro error de API**
</dt> <dd>

8

</dd> <dt>

**Error interno**
</dt> <dd>

9

</dd> </dl>

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Grupo Win32**](win32-group.md)
</dt> <dt>

[**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

