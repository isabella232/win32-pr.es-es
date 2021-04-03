---
description: El proveedor de clases WDM define la clase WMIBinaryMofResource en \\ el \\ espacio de nombres root WMI para admitir la tarea de realizar un seguimiento del estado de los datos en el repositorio WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Clase WMIBinaryMofResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908331"
---
# <a name="wmibinarymofresource-class"></a>Clase WMIBinaryMofResource

El proveedor de clases WDM define la clase **WMIBinaryMofResource** en \\ el \\ espacio de nombres root WMI para admitir la tarea de realizar un seguimiento del estado de los datos en el repositorio WMI.

## <a name="syntax"></a>Sintaxis

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>Miembros

La clase **WMIBinaryMofResource** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **WMIBinaryMofResource** tiene estas propiedades.

<dl> <dt>

**HighDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Mitad superior de la marca de fecha y hora.

</dd> <dt>

**LowDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Mitad inferior de la marca de fecha y hora.

</dd> <dt>

**MofProcessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Marca que indica si el archivo. mof se ha procesado por completo.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nombre del controlador habilitado para WDM que tiene un archivo MOF binario compilado correctamente en el repositorio WMI.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor de clases WDM crea una instancia de **WMIBinaryMofResource** para cada controlador WDM que proporciona un archivo MOF binario.

Siempre que WMI inicializa el proveedor, el proveedor compara la marca de tiempo con la marca de tiempo del archivo de imagen del controlador. Si las marcas de tiempo difieren, WMI vuelve a compilar el archivo MOF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                     |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proveedor de WDM](wdm-provider.md)
</dt> </dl>

 

