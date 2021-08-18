---
title: Método Delete de la Win32_TSAccount clase
description: El método Delete elimina la cuenta de usuario, grupo o equipo especificada.
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto , Win32_TSAccount clase
- Win32_TSAccount clase Servicios de Escritorio remoto método , Delete
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a320307838eb519e1f579e4c58be74a9231fcb3f88fe674dd89fc9e3bb5768ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058363"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a>Método Delete de la clase \_ TSAccount de Win32

El **método** Delete elimina la cuenta de usuario, grupo o equipo especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

