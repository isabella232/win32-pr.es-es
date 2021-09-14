---
description: Contiene métodos que obtienen el contenido sin procesar de los bloques de datos de 128 bytes estándar de Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x estándar.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073077"
---
# <a name="wmimonitordescriptormethods-class"></a>Clase WmiMonitorDescriptorMethods

La clase WMI **WmiMonitorDescriptorMethods** contiene métodos que obtienen el contenido sin procesar de los bloques de datos de 128 bytes estándar de definición de entrada de vídeo de Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x estándar.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La **clase WmiMonitorDescriptorMethods** tiene estos tipos de miembros:

-   [Métodos](#wmimonitordescriptormethods-class)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase WmiMonitorDescriptorMethods** tiene estos métodos.



| Método                                                                                           | Descripción                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Accede a los datos sin procesar de un bloque de descriptor edid v.1.x especificado.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase WmiMonitorDescriptorMethods** tiene estas propiedades.

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

Calificadores: **Clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




