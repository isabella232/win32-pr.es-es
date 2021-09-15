---
description: La función DeletePrinterDriverEx quita el nombre de controlador de impresora especificado de la lista de nombres de controladores admitidos en un servidor y elimina los archivos asociados al controlador. Esta función también puede eliminar versiones específicas del controlador.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Función DeletePrinterDriverEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359717"
---
# <a name="deleteprinterdriverex-function"></a>Función DeletePrinterDriverEx

La **función DeletePrinterDriverEx** quita el nombre de controlador de impresora especificado de la lista de nombres de controladores admitidos en un servidor y elimina los archivos asociados al controlador. Esta función también puede eliminar versiones específicas del controlador.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor del que se va a eliminar el controlador. Si este parámetro es **NULL,** la función elimina el controlador de impresora del equipo local.

</dd> <dt>

*pEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno del que se va a eliminar el controlador (por ejemplo, Windows NT x86, Windows IA64 o Windows x64). Si este parámetro es **NULL**, el nombre del controlador se elimina del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino ni del servidor de impresión).

</dd> <dt>

*pDriverName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del controlador que se eliminará.

</dd> <dt>

*dwDeleteFlag* \[ En\]
</dt> <dd>

Opciones para eliminar archivos y versiones del controlador. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                     | Significado                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**ELIMINACIÓN \_ DE DPD \_ VERSIÓN \_ ESPECÍFICA**</dt> </dl> | Elimina la versión especificada en *dwVersionFlag*. Esto no garantiza que el controlador se quite de la lista de controladores admitidos para el servidor.<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**ELIMINACIÓN \_ DE ARCHIVOS SIN \_ USAR DE \_ DPD**</dt> </dl>             | Quita los archivos de controlador no usados.<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**ELIMINACIÓN \_ DE TODOS LOS \_ ARCHIVOS DE \_ DPD**</dt> </dl>                      | Elimina el controlador solo si se pueden quitar todos sus archivos asociados. Se produce un error en la operación de eliminación si algún otro controlador instalado usa cualquiera de los archivos del controlador.<br/> |



 

Si no se especifica DPD DELETE SPECIFIC VERSION, la función elimina todas las versiones del controlador si \_ \_ ninguna está en \_ uso. Si no se especifica \_ DPD DELETE \_ UNUSED \_ FILES ni DPD DELETE ALL FILES, la función no \_ elimina los archivos de \_ \_ controlador.

</dd> <dt>

*dwVersionFlag* \[ En\]
</dt> <dd>

Versión del controlador que se va a eliminar. Este parámetro puede ser 0, 1, 2 o 3. Este parámetro solo se usa si *dwDeleteFlag incluye* la marca DELETE SPECIFIC VERSION de DPD. \_ \_ \_

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Antes de que la función elimine los archivos de controlador, llama a la función **DrvDriverEvent** del controlador, lo que permite al controlador quitar los archivos privados que no se usan. Para obtener más información **sobre DrvDriverEvent,** vea Microsoft Windows Driver Development Kit (DDK).

Si los archivos de controlador están cargados actualmente, la función los mueve a un directorio temporal y los marca para su eliminación en el reinicio.

Antes de **llamar a DeletePrinterDriverEx,** debe eliminar todos los objetos de impresora que usan el controlador de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterDriverExW** (Unicode) y **DeletePrinterDriverExA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

 




