---
description: Contiene la configuración utilizada durante las operaciones de mantenimiento.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Msvm_ServicingSettings clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79a0a6a141dfd027c0d9c44e70274853d908ce6afa6cae34e9f059b0a42ffdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950554"
---
# <a name="msvm_servicingsettings-class"></a>Clase Msvm \_ ServicingSettings

Contiene la configuración utilizada durante las operaciones de mantenimiento.

La sintaxis siguiente se Managed Object Format código MOF e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ ServicingSettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ ServicingSettings** tiene estas propiedades.

<dl> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene la versión de la definición de clase.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




