---
description: Agrega una conexión a la impresora especificada para el usuario actual y especifica los detalles de conexión.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Función AddPrinterConnection2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252339"
---
# <a name="addprinterconnection2-function"></a>Función AddPrinterConnection2

Agrega una conexión a la impresora especificada para el usuario actual y especifica los detalles de conexión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador de la ventana primaria en la que se mostrará el cuadro de diálogo si el sistema de impresión debe descargar un controlador de impresora del servidor de impresión para esta conexión.

</dd> <dt>

*pszName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en null constante que especifica el nombre de la impresora a la que el usuario actual desea conectarse.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Versión de la estructura a la que apunta *pConnectionInfo.* Actualmente, solo se define el nivel 1, por lo que el valor de *dwLevel* debe ser 1.

</dd> <dt>

*pConnectionInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura PRINTER CONNECTION INFO \_ \_ \_ 1.**](printer-connection-info-1.md) Consulte la sección Comentarios para obtener más información sobre este parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Cuando Windows Vista realiza una conexión a una impresora, puede que tenga que copiar los archivos del controlador de impresora desde el servidor al que está conectada la impresora. Si el usuario no tiene permiso para copiar archivos en la ubicación adecuada, se produce un error en la función **AddPrinterConnection2** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ ACCESS \_ DENIED.

Si los archivos del controlador de impresora se deben copiar desde el servidor de impresión, pero no se pueden copiar en modo silencioso debido a las directivas de grupo que están en vigor y la interfaz de usuario PRINTER CONNECTION NO está establecida en \_ \_ \_ *pConnectionInfo->dwFlags,* no se mostrará ningún cuadro de diálogo y se producirá un error en la llamada.

Si el controlador de impresora local se puede usar para representar trabajos de impresión para esta impresora y la versión del controlador local no debe coincidir con la versión del controlador de impresora en el servidor, establezca PRINTER CONNECTION MISMATCH en pConnectionInfo->dwFlags y asigne el puntero a una variable de cadena que contenga la ruta de acceso al controlador de impresora \_ \_ local a *pConnectionInfo->pszDriverName*. 

Una conexión de impresora que se establece mediante una llamada a **AddPrinterConnection2** se enumerará cuando se llame a [**EnumPrinters**](enumprinters.md) con *dwType* establecido en PRINTER \_ ENUM \_ CONNECTION.

No se admite la versión ANSI de esta **función, AddPrinterConnection2A,** y devuelve **ERROR NOT \_ \_ SUPPORTED**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

