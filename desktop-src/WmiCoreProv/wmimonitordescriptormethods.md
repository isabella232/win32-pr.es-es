---
description: Contiene métodos que obtienen el contenido sin procesar de la definición de entrada de vídeo de Video Electronics estándar Association (VESA) datos de identificación mejorada de la visualización extendida (E-EDID) v. 1. x 128 bits bloques de datos de bytes.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Clase WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678198"
---
# <a name="wmimonitordescriptormethods-class"></a>Clase WmiMonitorDescriptorMethods

La clase WMI **WmiMonitorDescriptorMethods** contiene métodos que obtienen el contenido sin procesar de la definición de entrada de vídeo de Video Electronics estándar Association (VESA) datos de identificación de presentación extendida mejorada (E-EDID) v. 1. x 128 bits bloques de datos de bytes.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Miembros

La clase **WmiMonitorDescriptorMethods** tiene estos tipos de miembros:

-   [Métodos](#wmimonitordescriptormethods-class)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **WmiMonitorDescriptorMethods** tiene estos métodos.



| Método                                                                                           | Descripción                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Obtiene acceso a los datos sin procesar de un bloque de descriptor de EDID v. 1. x especificado.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **WmiMonitorDescriptorMethods** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




