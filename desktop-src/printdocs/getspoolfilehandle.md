---
description: La función GetSpoolFileHandle recupera un identificador para el archivo spool asociado al trabajo enviado actualmente por la aplicación.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Función GetSpoolFileHandle (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 10b0b36333e51dfb5c831f6c74e00c6930ccbb9d1ce31646fed0d689abc7f639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686698"
---
# <a name="getspoolfilehandle-function"></a>Función GetSpoolFileHandle

La **función GetSpoolFileHandle** recupera un identificador para el archivo spool asociado al trabajo enviado actualmente por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora a la que se envió el trabajo. Debe ser el mismo identificador que se usó para enviar el trabajo. (Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve un identificador al archivo spool.

Si se produce un error en la función, devuelve **INVALID \_ HANDLE \_ VALUE**.

## <a name="remarks"></a>Comentarios

Con el identificador del archivo spool, la aplicación puede escribir en el archivo spool con llamadas a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguidas de [**CommitSpoolData**](commitspooldata.md).

La aplicación no debe llamar a [**ClosePrinter**](closeprinter.md) en *hPrinter* hasta que haya accedido al archivo spool por última vez. A continuación, [**debe llamar a CloseSpoolFileHandle**](closespoolfilehandle.md) seguido de **ClosePrinter**. Los intentos de acceder al identificador de archivo de cola después de que se haya cerrado *el hPrinter* original producirán un error incluso si el propio identificador de archivo no se ha cerrado. **CloseSpoolFileHandle producirá** un error si se llama primero a **ClosePrinter.**

Se producirá un error en esta función si se llama a antes de que el trabajo de impresión haya terminado de crear la cola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetSpoolFileHandleW** (Unicode) y **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 

