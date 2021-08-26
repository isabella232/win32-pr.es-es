---
description: Representa un controlador de impresora del que dependen otros controladores de impresora.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: CORE_PRINTER_DRIVER estructura (Winspool.h)
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
ms.openlocfilehash: 18ac3dba88d9cf781393b01b6594777426b7195e6f68afa0fd00a5bddb01f129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950405"
---
# <a name="core_printer_driver-structure"></a>CORE \_ PRINTER \_ DRIVER (Estructura DEL CONTROLADOR DE IMPRESORA PRINCIPAL)

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

Identificador de versión de la versión más reciente del controlador de impresora principal.

</dd> <dt>

**szPackageID \[ MAX \_ PATH\]**
</dt> <dd>

Ruta de acceso al paquete de controladores que contiene el controlador de impresora principal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura puede representar el controlador base de un fabricante del que dependen los controladores de varios modelos de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ CORE \_ PRINTER \_ DRIVERW** (Unicode) e **\_ CORE PRINTER \_ \_ DRIVERA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




