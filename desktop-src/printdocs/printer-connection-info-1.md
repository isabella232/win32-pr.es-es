---
description: Representa información sobre una conexión a una impresora.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: PRINTER_CONNECTION_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b9adbe18d3f75062a67440fd7f7586c4336323ff3035416f3ad9799f5e34a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033903"
---
# <a name="printer_connection_info_1-structure"></a>Estructura PRINTER \_ CONNECTION \_ INFO \_ 1

Representa información sobre una conexión a una impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwFlags**
</dt> <dd>

Se definen los valores siguientes:



| Value                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR DE \_ COINCIDENCIA DE CONEXIÓN DE IMPRESORA \_ (0x00000020) | Si se establece esta marca de bits, la conexión de la impresora no coincide. El usuario puede proporcionar un controlador de impresión local como *pszDriverName* y usarlo para realizar la representación en lugar de usar el controlador instalado en la impresora del servidor a la que está conectado el usuario.<br/>                                                                                                                                                                                                                                    |
| CONEXIÓN \_ DE IMPRESORA SIN INTERFAZ DE USUARIO \_ \_ (0x00000040)   | Si se establece esta marca de bits, esta llamada no puede mostrar un cuadro de diálogo. Si se debe mostrar un cuadro de diálogo para instalar un controlador de impresora desde el servidor y se establece esta marca de bits, el controlador de impresora no se instalará, no se agregará la conexión de impresora y se producirá un error en la llamada.<br/> **Windows 7:** En Windows 7 y versiones posteriores de Windows, si esta marca está establecida y el usuario se ejecuta en modo con privilegios elevados, no se mostrará el cuadro de diálogo Do **you trust this printer?** (¿Confía en esta impresora?).<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Puntero al nombre del controlador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




