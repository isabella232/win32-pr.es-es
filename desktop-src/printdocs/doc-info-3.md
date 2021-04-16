---
description: La \_ estructura doc info \_ 3 describe un documento que se va a imprimir.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Estructura de DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716032"
---
# <a name="doc_info_3-structure"></a>Estructura de DOC \_ info \_ 3

La estructura **doc \_ info \_ 3** describe un documento que se va a imprimir.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pDocName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de un archivo de salida.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar el documento.

</dd> <dt>

**dwFlags**
</dt> <dd>

Marcas. Actualmente, puede ser **null** o el siguiente.



| Marca                 | Significado                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| escritura de DI \_ MEMORYMAP \_ | Hace que [**StartDocPrinter**](startdocprinter.md) no use [**AddJob**](addjob.md) y [**ScheduleJob**](schedulejob.md) para la impresión local. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La \_ \_ configuración de escritura de di MEMORYMAP en la **información de documento \_ \_ 3** es una optimización. Esto permite que GDI asigne los archivos de cola de impresión en la aplicación y acelere la grabación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información de documento \_ \_ 3W** (Unicode) y **\_ información de documento \_ \_ 3A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




