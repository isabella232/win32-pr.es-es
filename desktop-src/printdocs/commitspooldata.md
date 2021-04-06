---
description: La función CommitSpoolData notifica al administrador de trabajos de impresión que se ha escrito una cantidad de datos especificada en un archivo de cola especificado y está listo para ser representada.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Función CommitSpoolData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909378"
---
# <a name="commitspooldata-function"></a>CommitSpoolData función)

La función **CommitSpoolData** notifica al administrador de trabajos de impresión que se ha escrito una cantidad de datos especificada en un archivo de cola especificado y está listo para ser representada.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora a la que se envió el trabajo. Debe ser el mismo identificador que se usó para obtener *hSpoolFile* con [**GetSpoolFileHandle**](getspoolfilehandle.md).

</dd> <dt>

*hSpoolFile* \[ de\]
</dt> <dd>

Identificador del archivo de cola que se va a cambiar. En la primera llamada de **CommitSpoolData**, debe ser el mismo identificador devuelto por [**GetSpoolFileHandle**](getspoolfilehandle.md). Las llamadas subsiguientes a **CommitSpoolData** deben pasar el identificador devuelto por la llamada anterior. Vea la sección Comentarios.

</dd> <dt>

*cbCommit* 
</dt> <dd>

Número de bytes confirmados en el administrador de trabajos de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve un identificador para el archivo de cola.

Si se produce un error en la función, devuelve un valor de identificador no válido \_ \_ .

## <a name="remarks"></a>Observaciones

Las aplicaciones que envían un trabajo de impresión del administrador de trabajos en cola pueden llamar a [**GetSpoolFileHandle**](getspoolfilehandle.md) y, a continuación, escribir los datos directamente en el identificador de la cola de impresión mediante una llamada a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Para notificar al administrador de trabajos de impresión que el archivo contiene datos que están listos para su representación, la aplicación debe llamar a **CommitSpoolData** y proporcionar el número de bytes disponibles.

Si se llama a **CommitSpoolData** varias veces, cada llamada debe usar el identificador de archivo de cola de impresión devuelto por la llamada anterior. Cuando no se escriban más datos en el archivo de cola de impresión, se debe llamar a [**CloseSpoolFileHandle**](closespoolfilehandle.md) para el identificador de archivo devuelto por la última llamada a **CommitSpoolData**.

Antes de llamar a **CommitSpoolData**, las aplicaciones deben establecer el puntero de archivo en la posición que tenía antes de escribir los datos en el archivo. En el proceso de representar los datos en el archivo del administrador de trabajos de impresión, el administrador de trabajos de impresión moverá el puntero del archivo de cola de *cbCommit* bytes del valor actual del puntero de archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 

