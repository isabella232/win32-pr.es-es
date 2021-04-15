---
description: Representa un controlador de impresora del que dependen otros controladores de impresora.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Estructura de CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648375"
---
# <a name="core_printer_driver-structure"></a>Estructura del controlador de \_ impresora principal \_

Representa un controlador de impresora del que dependen otros controladores de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CoreDriverGUID**
</dt> <dd>

GUID del controlador de impresora principal.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Fecha y hora de la versión más reciente del controlador de impresora principal.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

El ID. de versión de la versión más reciente del controlador de impresora principal.

</dd> <dt>

**\[ruta de acceso máxima de szPackageID \_\]**
</dt> <dd>

La ruta de acceso al paquete de controladores que contiene el controlador de impresora principal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura puede representar el controlador base de un fabricante en el que dependen los controladores de varios modelos de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Core \_ Printer \_ DRIVERW** (Unicode) y **\_ Core \_ Printer \_ drivera** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




