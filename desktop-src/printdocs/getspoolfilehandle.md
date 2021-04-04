---
description: La función GetSpoolFileHandle recupera un identificador para el archivo de cola asociado al trabajo enviado actualmente por la aplicación.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Función GetSpoolFileHandle (winspool. h)
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
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083362"
---
# <a name="getspoolfilehandle-function"></a>GetSpoolFileHandle función)

La función **GetSpoolFileHandle** recupera un identificador para el archivo de cola asociado al trabajo enviado actualmente por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora a la que se envió el trabajo. Debe ser el mismo identificador que se usó para enviar el trabajo. (Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve un identificador para el archivo de cola.

Si se produce un error en la función, devuelve un **\_ \_ valor de identificador no válido**.

## <a name="remarks"></a>Observaciones

Con el identificador del archivo de cola de impresión, la aplicación puede escribir en el archivo de cola de impresión con llamadas a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguido de [**CommitSpoolData**](commitspooldata.md).

La aplicación no debe llamar a [**ClosePrinter**](closeprinter.md) en *hPrinter* hasta que haya tenido acceso por última vez al archivo de cola de impresión. Después, debe llamar a [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguido de **ClosePrinter**. Los intentos de obtener acceso al identificador de la cola de impresión una vez cerrado el *hPrinter* original producirán un error aunque no se haya cerrado el propio identificador de archivo. **CloseSpoolFileHandle** producirá un error si se llama primero a **ClosePrinter** .

Esta función producirá un error si se llama antes de que el trabajo de impresión haya terminado de poner en cola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetSpoolFileHandleW** (Unicode) y **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 

