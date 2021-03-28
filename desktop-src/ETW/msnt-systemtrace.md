---
description: Clase primaria de la que se derivan todas las clases de seguimiento de eventos del sistema. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984570"
---
# <a name="msnt_systemtrace-class"></a>MSNT \_ SystemTrace (clase)

Clase primaria de la que se derivan todas las clases de seguimiento de eventos del sistema.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Miembros

La clase **MSNT \_ SystemTrace** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSNT \_ SystemTrace** tiene estas propiedades.

<dl> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **DefineValues {" \_ \_ \_ proceso de marca de seguimiento de eventos", " \_ \_ \_ subproceso de marca de seguimiento de eventos", " \_ carga de imagen de \_ marca de seguimiento de eventos \_ \_ ", " \_ \_ \_ \_ contadores de proceso de marca de seguimiento de eventos", "marca de seguimiento de eventos \_ \_ \_ CSWITCH", "marca de seguimiento de eventos \_ \_ \_ DPC", " \_ \_ interrupción de la marca \_ de seguimiento marca de seguimiento de \_ \_ \_ eventos \_ \_ \_ \_ e e/s de disco", "marca de seguimiento de eventos \_ \_ \_ \_ \_ e/s de archivo de disco", "marca de seguimiento de eventos \_ \_ \_ \_ de e/s de disco \_ ", " \_ distribuidor de marcas de seguimiento de eventos", "errores de página de la marca de seguimiento de eventos", "error de la memoria de la marca de seguimiento de eventos \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ " \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ registro de marca de seguimiento de eventos "," marca de seguimiento de eventos \_ \_ \_ ALPC "," marca de seguimiento de evento \_ \_ \_ Split \_ IO "," \_ controlador de marca de seguimiento de eventos \_ \_ "," \_ \_ Perfil de marca de seguimiento de eventos \_ "," \_ \_ \_ \_ e/s de archivo de marca de seguimiento de eventos "," seguimiento de eventos \_ marcas de \_ \_ e/s de archivo de marca \_ \_ "}**, **ValueMap {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**
</dt> </dl>

Habilita la marca que indica los proveedores de kernel habilitados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



 

 




