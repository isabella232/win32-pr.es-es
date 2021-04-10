---
description: SetShareInfo&\# 8194; El método de clase WMI establece los parámetros de un recurso compartido.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Método SetShareInfo de la clase Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275101"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Método SetShareInfo de la \_ clase de recursos compartidos de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** establece los parámetros de un recurso compartido.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaximumAllowed* \[ en, opcional\]
</dt> <dd>

Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.

Ejemplo: 10. Este parámetro es opcional.

</dd> <dt>

*Descripción* \[ de en, opcional\]
</dt> <dd>

Comentario opcional para describir el recurso que se está compartiendo.

</dd> <dt>

*Acceso a* \[ en, opcional\]
</dt> <dd>

Descriptor de seguridad para permisos de nivel de usuario. Un descriptor de seguridad contiene información sobre el permiso, el propietario y las capacidades de acceso del recurso. Para obtener más información, [**vea \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Nombre no válido** (9)
</dt> <dt>

**Nivel no válido** (10)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Recurso compartido duplicado** (22)
</dt> <dt>

**Ruta de acceso redirigida** (23)
</dt> <dt>

**Dispositivo o directorio desconocido** (24)
</dt> <dt>

**No se encontró el nombre de red** (25)
</dt> <dt>

**Otro** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El método **SetShareInfo** es un método de objeto dinámico y se usa en una aparición de esta clase.

Solo los miembros del grupo local Administradores o operadores de cuenta, o los que tengan la pertenencia a un grupo de operador de servidor o de comunicación pueden ejecutar correctamente **SetShareInfo**. El operador Print solo puede establecer colas de impresora. El operador de comunicación solo puede establecer colas de dispositivos de comunicación.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de PowerShell actualiza el nombre del recurso compartido **newShare** .


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



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

[**\_Recurso compartido de Win32**](win32-share.md)
</dt> </dl>

 

