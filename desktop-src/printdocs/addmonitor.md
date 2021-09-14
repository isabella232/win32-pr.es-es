---
description: La función AddMonitor instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Función AddMonitor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252356"
---
# <a name="addmonitor-function"></a>Función AddMonitor

La **función AddMonitor** instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que se debe instalar el monitor. En el caso de los sistemas que solo admiten la instalación local de monitores, esta cadena debe ser **NULL.**

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que *apunta pMonitors.* Este valor debe ser 2.

</dd> <dt>

*pMonitors* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ MONITOR INFO \_ 2.**](monitor-info-2.md) Si el **miembro pEnvironment** de la estructura *pMonitors* es **NULL,** se usa el entorno actual del autor de la llamada (cliente), no del destino (servidor).

Tenga en cuenta que se producirá un error en la llamada si el entorno no coincide con el entorno del servidor, es decir, solo puede agregar un monitor escrito para la arquitectura del servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El autor de la llamada debe [tener seLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes de que una aplicación llame **a la función AddMonitor,** todos los archivos requeridos por el monitor deben copiarse en el directorio SYSTEM32.

Para determinar los monitores de puerto que están instalados actualmente, llame a la [**función EnumMonitors.**](enummonitors.md)

Para quitar un monitor agregado por **AddMonitor,** llame a [**la función DeleteMonitor.**](deletemonitor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddMonitorW** (Unicode) y **AddMonitorA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeleteMonitor**](deletemonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**INFORMACIÓN \_ DE SUPERVISIÓN \_ 2**](monitor-info-2.md)
</dt> </dl>

 

