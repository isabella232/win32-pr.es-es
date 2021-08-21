---
description: Enumera los modos de origen admitidos para un monitor de vídeo en su descriptor de monitor, si existe alguno.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Clase WmiMonitorListedSupportedSourceModes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ca942fce42388eaeb2eb90b7b7ecd992dd6df39bca554bb63bbc55fb6bbb867a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821470"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a>Clase WmiMonitorListedSupportedSourceModes

**WmiMonitorListedSupportedSourceModes** enumera los modos de origen admitidos para un monitor de vídeo en su descriptor de monitor, si existe alguno. En el caso de los monitores que no tienen ninguna descripción, esta lista de modos se genera en función del tipo de monitor, según lo especificado por el controlador de bus de supervisión.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a>Miembros

La **clase WmiMonitorListedSupportedSourceModes** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorListedSupportedSourceModes** tiene estas propiedades.

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

</dd> <dt>

**MonitorSourceModes**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz VideoModeDescriptor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Enumera los modos de origen del monitor representados por instancias de la [**clase VideoModeDescriptor.**](videomodedescriptor.md)

</dd> <dt>

**NumOfMonitorSourceModes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de monitores admitidos en la lista.

</dd> <dt>

**PreferredMonitorSourceModeIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Índice de modo de origen de monitor preferido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




