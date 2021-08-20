---
description: La función SetPrinter establece los datos de una impresora especificada o establece el estado de la impresora especificada al pausar la impresión, reanudar la impresión o borrar todos los trabajos de impresión.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Función SetPrinter (WinSpool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: de26915b09cd49e4742b762105d4b9ad4868110e79debfa537c63077d24d1f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056157"
---
# <a name="setprinter-function"></a>Función SetPrinter

La **función SetPrinter** establece los datos de una impresora especificada o establece el estado de la impresora especificada al pausar la impresión, reanudar la impresión o borrar todos los trabajos de impresión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora. Use la [**función OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de datos que la función almacena en el búfer al que apunta *pPrinter.* Si el *parámetro Command* no es igual a cero, el *parámetro Level* debe ser cero.

Este valor puede ser 0, 2, 3, 4, 5, 6, 7, 8 o 9.

</dd> <dt>

*pPrinter* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene los datos que se establecerán para la impresora o que contiene información para el comando especificado por el *parámetro Command.* El tipo de datos del búfer viene determinado por el valor de *Level*.



| Nivel                                                                                                | Estructura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Si el *parámetro Command* es PRINTER CONTROL **SET \_ \_ \_ STATUS**, *pPrinter* debe contener un valor **DWORD** que especifique el nuevo estado de la impresora que se va a establecer. Para obtener una lista de los valores de estado posibles, vea el **miembro Status** de la estructura PRINTER [**INFO \_ \_ 2.**](printer-info-2.md) Tenga en cuenta **que PRINTER \_ STATUS \_ PAUSED** y **PRINTER STATUS PENDING \_ \_ \_ DELETION** no son valores de estado válidos para establecer.<br/> Si *Level* es 0, pero el parámetro *Command* no es PRINTER CONTROL **\_ SET \_ \_ STATUS**, *pPrinter* debe ser **NULL.**<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 2**](printer-info-2.md) que contiene información detallada sobre la impresora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 3**](printer-info-3.md) que contiene la información de seguridad de la impresora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 4**](printer-info-4.md) que contiene información de impresora mínima, incluido el nombre de la impresora, el nombre del servidor y si la impresora es remota o local.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 5 que**](printer-info-5.md) contiene información de impresora, como atributos de impresora y valores de tiempo de espera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 6**](printer-info-6.md) que especifica el valor de estado de una impresora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 7.**](printer-info-7.md) El *miembro dwAction* de esta estructura indica si **SetPrinter** debe publicar, anular la publicación, volver a publicar o actualizar los datos de la impresora en el servicio de directorio.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 8**](printer-info-8.md) que especifica la configuración de impresora predeterminada global.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Estructura [**PRINTER \_ INFO \_ 9**](printer-info-9.md) que especifica la configuración predeterminada de la impresora por usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*Comando* \[ En\]
</dt> <dd>

la acción que se va a realizar.

Si el *parámetro Level* es distinto de cero, establezca el valor de este parámetro en cero. En este caso, la impresora conserva su estado actual y la función vuelve a configurar los datos de la impresora según lo especificado por los parámetros *Level* y *pPrinter.*

Si el *parámetro Level* es cero, establezca el valor de este parámetro en uno de los valores siguientes.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**PAUSA \_ DEL CONTROL DE \_ IMPRESORA**</dt> </dl>                 | Pausar la impresora.<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**PURGA \_ DEL CONTROL DE \_ IMPRESORA**</dt> </dl>                 | Elimine todos los trabajos de impresión de la impresora.<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**REANUDACIÓN \_ DEL CONTROL \_ DE IMPRESORA**</dt> </dl>              | Reanudar una impresora en pausa.<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**ESTADO DEL \_ CONJUNTO DE CONTROLES DE \_ \_ IMPRESORA**</dt> </dl> | Establezca el estado de la impresora.<br/> Establezca el *parámetro pPrinter* en un puntero a un **valor DWORD** que especifique el nuevo estado de la impresora.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Si *El nivel* es 7 y se produjo un error en la acción de publicación, **SetPrinter** devuelve ERROR **\_ E/S \_ PENDIENTE** e intenta completar la acción en segundo plano. Si *Level* es 7 y se produjo un error en la acción de actualización, **SetPrinter** devuelve **ERROR FILE NOT \_ \_ \_ FOUND**.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

No puede usar **SetPrinter para** cambiar la impresora predeterminada.

Para modificar la configuración actual de la impresora, llame a la función [**GetPrinter**](getprinter.md) para recuperar la configuración actual en una estructura [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) modifique los miembros de esa estructura según sea necesario y, a continuación, llame a **SetPrinter**.

La **función SetPrinter** omite los miembros **pServerName**, **AveragePPM,** **Status** y **cJobs** de una [**estructura PRINTER INFO \_ \_ 2.**](printer-info-2.md)

Al pausar una impresora, se suspende la programación de todos los trabajos de impresión de esa impresora, excepto el trabajo de impresión que se puede imprimir actualmente. Los trabajos de impresión se pueden enviar a una impresora en pausa, pero no se programará ningún trabajo para imprimir en esa impresora hasta que se reanude la impresión. Si se borra una impresora, se eliminan todos los trabajos de impresión de esa impresora, excepto el trabajo de impresión actual.

Si usa **SetPrinter** para modificar la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predeterminada de una impresora (estableciendo globalmente los valores predeterminados de la impresora), primero debe llamar a la función [**DocumentProperties**](documentproperties.md) para validar la estructura **DEVMODE.**

Para las estructuras [**PRINTER \_ INFO \_ 2**](printer-info-2.md) e [**PRINTER INFO \_ \_ 3**](printer-info-3.md) que contienen un puntero a un descriptor de seguridad, la función solo puede establecer los componentes del descriptor de seguridad que el autor de la llamada tiene permiso para modificar. Para establecer determinados componentes de descriptor de seguridad, debe especificar los derechos de acceso necesarios al llamar a la función [**OpenPrinter**](openprinter.md) o [**OpenPrinter2**](openprinter2.md) para recuperar un identificador de la impresora. En la tabla siguiente se muestran los derechos de acceso necesarios para modificar los distintos componentes del descriptor de seguridad.



| Permiso de acceso            | Componente descriptor de seguridad             |
|------------------------------|-------------------------------------------|
| **PROPIETARIO DE \_ ESCRITURA**             | Propietario<br/> Grupo primario<br/> |
| **ESCRIBIR \_ DAC**               | Lista de control de acceso discrecional (DACL)  |
| **ACCESO A \_ LA SEGURIDAD DEL \_ SISTEMA** | Lista de control de acceso del sistema (SACL)         |



 

Si el descriptor de seguridad contiene un componente que el autor de la llamada no tiene el derecho de acceso para modificar, se produce un error **en SetPrinter.** Los componentes de un descriptor de seguridad que no desea modificar deben ser **NULL** o no estar presentes, según corresponda. Si no desea modificar el descriptor de seguridad y llama a **SetPrinter** con una estructura [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) establezca el miembro **pSecurityDescriptor** de esa estructura en **NULL.**

El Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para el uso compartido de archivos e impresión. Si un administrador de la máquina llama a **SetPrinter,** habilita la excepción. Si lo llama un usuario que no es administrador y la excepción aún no se ha habilitado, se produce un error en la llamada.

Puede usar el nivel 7 con la estructura [**PRINTER \_ INFO \_ 7**](printer-info-7.md) para publicar, anular la publicación o actualizar los datos del servicio de directorio de la impresora. Los datos del servicio de directorio de una impresora incluyen todos los datos almacenados en las claves SPLDS mediante llamadas a la \_ \* [**función SetPrinterDataEx**](setprinterdataex.md) de la impresora. Antes de **llamar a SetPrinter**, establezca el miembro **pszObjectGUID** de **PRINTER INFO \_ \_ 7** en **NULL** y establezca el *miembro dwAction* en uno de los valores siguientes.



| Value                             | Descripción                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PUBLICACIÓN DE DSPRINT \_**<br/>   | Publica los datos del servicio de directorio.<br/>                                                                                                                                                                                                                                                                                                                                        |
| **PUBLICACIÓN DE \_ DSPRINT**<br/> | Los datos del servicio de directorio de la impresora no se publican y, a continuación, se publican de nuevo, actualizando todas las propiedades de la impresora publicada. Volver a publicar también cambia el GUID de la impresora publicada. Use este valor si sospecha que los datos publicados de la impresora se han dañado.<br/>                                                                                         |
| **DSPRINT \_ UNPUBLISH**<br/> | Despublica los datos del servicio de directorio.<br/>                                                                                                                                                                                                                                                                                                                                      |
| **ACTUALIZACIÓN DE \_ DSPRINT**<br/>    | Actualiza los datos del servicio de directorio. Esto es igual que **DSPRINT \_ PUBLISH,** salvo que **SetPrinter** produce un error con **ERROR FILE NOT \_ \_ \_ FOUND** si la impresora aún no está publicada.<br/> Use **DSPRINT \_ UPDATE para** actualizar las propiedades publicadas, pero no forzar la publicación. Los controladores de impresora siempre **deben usar DSPRINT \_ UPDATE en** lugar de **DSPRINT \_ PUBLISH.**<br/> |



 

**DSPRINT \_ PENDING** no es un valor *dwAction* válido para **SetPrinter.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>WinSpool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinSpool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPrinterW** (Unicode) y **SetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 5**](printer-info-5.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 6**](printer-info-6.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 7**](printer-info-7.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 8**](printer-info-8.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 9**](printer-info-9.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




