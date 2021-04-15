---
description: Contiene los valores utilizados durante las operaciones de mantenimiento.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Msvm_ServicingSettings (clase)
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
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497705"
---
# <a name="msvm_servicingsettings-class"></a>MSVM \_ ServicingSettings (clase)

Contiene los valores utilizados durante las operaciones de mantenimiento.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ServicingSettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ServicingSettings** tiene estas propiedades.

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




