---
description: Representa información sobre una conexión a una impresora.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Estructura de PRINTER_CONNECTION_INFO_1 (winspool. h)
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
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814867"
---
# <a name="printer_connection_info_1-structure"></a>Estructura de la información de conexión de impresora \_ \_ \_ 1

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
| Conexión de impresora \_ \_ no coincidente (0x00000020) | Si se establece esta marca de bits, la conexión de impresora no coincide. El usuario puede proporcionar un controlador de impresión local como *pszDriverName* y usarlo para realizar la representación en lugar de usar el controlador instalado en la impresora del servidor a la que está conectado el usuario.<br/>                                                                                                                                                                                                                                    |
| Conexión de impresora \_ \_ sin \_ interfaz de usuario (0x00000040)   | Si se establece esta marca de bits, esta llamada no puede mostrar un cuadro de diálogo. Si se debe mostrar un cuadro de diálogo para instalar un controlador de impresora desde el servidor y esta marca de bits está establecida, el controlador de impresora no se instalará, la conexión de impresora no se agregará y se producirá un error en la llamada.<br/> **Windows 7:** En Windows 7 y versiones posteriores de Windows, si se establece esta marca y el usuario se ejecuta en modo con privilegios elevados, no se mostrará el cuadro de diálogo **¿confía en esta impresora?** .<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Puntero al nombre del controlador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




