---
title: Win32_SessionDirectoryVirtualDesktopServer (clase)
description: Representa un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto) unido a un agente de sesión.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryVirtualDesktopServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079090"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a>\_Clase Win32 SessionDirectoryVirtualDesktopServer

Representa un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto) unido a un agente de sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionDirectoryVirtualDesktopServer de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionDirectoryVirtualDesktopServer de Win32** tiene estas propiedades.

<dl> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre DNS del servidor host de virtualización de escritorio remoto. Este nombre tiene el formato "*MachineName*. *Dominio*. com ".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

