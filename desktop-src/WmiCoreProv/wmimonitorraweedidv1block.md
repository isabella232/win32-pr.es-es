---
description: Representa los datos sin procesar de una estructura de datos mejorados de identificación de pantalla extendida (E-EDID) de Video Electronics Standard Association (VESA).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Clase WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 72b82f2c6eb967f39823d5b56174bb82e7503ee56f676ffb49b65822ec435936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821150"
---
# <a name="wmimonitorraweedidv1block-class"></a>Clase WmiMonitorRawEEdidV1Block

La clase WMI **WmiMonitorRawEEdidV1Block** representa los datos sin procesar de una estructura de datos mejorados de identificación de pantalla extendida (E-EDID) de Video Electronics Standard Association (VESA). Esta estructura de datos de 128 bytes contiene información que describe la configuración óptima para una presentación.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a>Miembros

La **clase WmiMonitorRawEEdidV1Block** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorRawEEdidV1Block** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**Contenido**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de 128 bytes que contiene el contenido del bloque sin formato.

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identidad del bloque de datos.

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

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de bloque de datos. En la tabla siguiente se enumeran los valores posibles que se pueden devolver.



| Value                                                                                 | Significado                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | No inicializado<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Bloque base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mapa de bloques EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Otros<br/>           |



 

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
</dt> <dt>

[**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




