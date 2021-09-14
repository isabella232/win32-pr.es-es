---
description: El proveedor de clases WDM define la clase WMIBinaryMofResource en el espacio de nombres wmi raíz para admitir la tarea de realizar un seguimiento del estado de los datos en el \\ \\ repositorio WMI.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073098"
---
# <a name="wmibinarymofresource-class"></a>Clase WMIBinaryMofResource

El proveedor de clases WDM define la clase **WMIBinaryMofResource** en el espacio de nombres wmi raíz para admitir la tarea de realizar un seguimiento del estado de los datos en el \\ \\ repositorio WMI.

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

## <a name="members"></a>Members

La **clase WMIBinaryMofResource** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WMIBinaryMofResource** tiene estas propiedades.

<dl> <dt>

**HighDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

La mitad alta de la marca de fecha y hora.

</dd> <dt>

**LowDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Mitad baja de la marca de fecha y hora.

</dd> <dt>

**MofProcessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Marca que indica si el archivo .mof se procesó completamente.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nombre del controlador habilitado para WDM que tiene un archivo MOF binario compilado correctamente en el repositorio WMI.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor de clases WDM crea una instancia de **WMIBinaryMofResource** para cada controlador WDM que proporciona un archivo MOF binario.

Cada vez que WMI inicializa el proveedor, el proveedor compara la marca de tiempo con la marca de tiempo del archivo de imagen del controlador. Si las marcas de tiempo difieren, WMI vuelve a compilar el archivo MOF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                     |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Wmi.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Proveedor wdm](wdm-provider.md)
</dt> </dl>

 

