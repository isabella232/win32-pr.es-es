---
description: La función CloseSpoolFileHandle cierra un identificador a un archivo de cola asociado al trabajo de impresión enviado actualmente por la aplicación.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Función CloseSpoolFileHandle (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168102"
---
# <a name="closespoolfilehandle-function"></a>Función CloseSpoolFileHandle

La **función CloseSpoolFileHandle** cierra un identificador a un archivo de cola asociado al trabajo de impresión enviado actualmente por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora a la que se envió el trabajo. Debe ser el mismo identificador que se usó para obtener *hSpoolFile* con [**GetSpoolFileHandle.**](getspoolfilehandle.md)

</dd> <dt>

*hSpoolFile* \[ En\]
</dt> <dd>

Identificador del archivo de cola de trabajos que se va a cerrar. Si [**no se ha llamado a CommitSpoolData**](commitspooldata.md) desde que se llamó a [**GetSpoolFileHandle,**](getspoolfilehandle.md) debe ser el mismo identificador devuelto por **GetSpoolFileHandle.** De lo contrario, debe ser el identificador devuelto por la llamada más reciente a **CommitSpoolData**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE**, si se realiza correctamente, FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

La aplicación no debe llamar a [**ClosePrinter**](closeprinter.md) en *hPrinter* hasta que haya accedido al archivo spool por última vez. A continuación, **debe llamar a CloseSpoolFileHandle** seguido de **ClosePrinter**. Los intentos de acceder al identificador de archivo de cola después de que se haya cerrado *el hPrinter* original producirán un error incluso si el propio identificador de archivo no se ha cerrado. **CloseSpoolFileHandle producirá** un error si se llama primero a **ClosePrinter.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> </dl>

 

 




