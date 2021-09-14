---
description: La función CommitSpoolData notifica al administrador de trabajos de impresión que una cantidad especificada de datos se ha escrito en un archivo de cola especificado y está lista para representarse.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Función CommitSpoolData (Winspool.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168098"
---
# <a name="commitspooldata-function"></a>Función CommitSpoolData

La **función CommitSpoolData** notifica al administrador de trabajos de impresión que una cantidad especificada de datos se ha escrito en un archivo de cola especificado y está lista para representarse.

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

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora a la que se envió el trabajo. Debe ser el mismo identificador que se usó para obtener *hSpoolFile* con [**GetSpoolFileHandle.**](getspoolfilehandle.md)

</dd> <dt>

*hSpoolFile* \[ En\]
</dt> <dd>

Identificador del archivo de cola de trabajos que se va a cambiar. En la primera llamada de **CommitSpoolData**, debe ser el mismo identificador devuelto por [**GetSpoolFileHandle.**](getspoolfilehandle.md) Las llamadas posteriores **a CommitSpoolData** deben pasar el identificador devuelto por la llamada anterior. Vea la sección Comentarios.

</dd> <dt>

*cbCommit* 
</dt> <dd>

Número de bytes confirmados en el colador de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve un identificador al archivo spool.

Si se produce un error en la función, devuelve INVALID \_ HANDLE \_ VALUE.

## <a name="remarks"></a>Observaciones

Las aplicaciones que envían un trabajo de impresión de cola pueden llamar a [**GetSpoolFileHandle**](getspoolfilehandle.md) y, a continuación, escribir datos directamente en el identificador de archivo de cola mediante una llamada [**a WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Para notificar al cola de impresión que el archivo contiene datos que están listos para representarse, la aplicación debe llamar a **CommitSpoolData** y proporcionar el número de bytes disponibles.

Si **se llama a CommitSpoolData** varias veces, cada llamada debe usar el identificador de archivo spool devuelto por la llamada anterior. Cuando no se escribirán más datos en el archivo spool, se debe llamar a [**CloseSpoolFileHandle**](closespoolfilehandle.md) para el identificador de archivo devuelto por la última llamada a **CommitSpoolData**.

Antes de **llamar a CommitSpoolData,** las aplicaciones deben establecer el puntero de archivo en la posición que tenía antes de escribir datos en el archivo. En el proceso de representación de los datos en el archivo de cola de impresión, el administrador de trabajos de impresión moverá el puntero de archivo de cola *cbCommit* bytes del valor actual del puntero de archivo.

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

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 

