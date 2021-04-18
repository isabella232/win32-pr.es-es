---
description: La función SetPrinter establece los datos de una impresora especificada o establece el estado de la impresora especificada mediante la pausa de la impresión, la reanudación de la impresión o la eliminación de todos los trabajos de impresión.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Función SetPrinter (WinSpool. h)
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
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716481"
---
# <a name="setprinter-function"></a>SetPrinter función)

La función **SetPrinter** establece los datos de una impresora especificada o establece el estado de la impresora especificada mediante la pausa de la impresión, la reanudación de la impresión o la eliminación de todos los trabajos de impresión.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora. Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

El tipo de datos que la función almacena en el búfer al que apunta *pPrinter*. Si el parámetro de *comando* no es igual a cero, el parámetro *LEVEL* debe ser cero.

Este valor puede ser 0, 2, 3, 4, 5, 6, 7, 8 o 9.

</dd> <dt>

*pPrinter* \[ de\]
</dt> <dd>

Puntero a un búfer que contiene los datos que se van a establecer para la impresora o que contienen información para el comando especificado por el parámetro de *comando* . El tipo de datos del búfer viene determinado por el valor de *LEVEL*.



| Nivel                                                                                                | Estructura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | Si el parámetro de *comando* es el estado del conjunto de control de la impresora, *pPrinter* debe contener un valor **DWORD** que especifique el nuevo estado de la impresora que se va a establecer. **\_ \_ \_** Para obtener una lista de los valores de estado posibles, vea el miembro **status** de la estructura de la [**impresora \_ info \_ 2**](printer-info-2.md) . Tenga en cuenta que el estado de la **impresora en \_ \_ pausa** y el estado de la **impresora \_ pendiente de \_ \_ eliminación** no son valores de estado válidos para establecer.<br/> Si el *nivel* es 0, pero el parámetro del *comando* no es el estado del  conjunto de control de la impresora, pPrinter debe ser **null**. **\_ \_ \_**<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que contiene información detallada acerca de la impresora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 3**](printer-info-3.md) que contiene la información de seguridad de la impresora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 4**](printer-info-4.md) que contiene la información de impresora mínima, incluido el nombre de la impresora, el nombre del servidor y si la impresora es remota o local.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Una estructura de información de impresora [**\_ \_ 5**](printer-info-5.md) que contiene información de la impresora, como los atributos de impresora y la configuración de tiempo de espera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Estructura de la información de la [**impresora \_ \_ 6**](printer-info-6.md) que especifica el valor de estado de una impresora.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Estructura de la información de la [**impresora \_ \_ 7**](printer-info-7.md) . El miembro *dwAction* de esta estructura indica si **SetPrinter** debe publicar, anular la publicación, volver a publicar o actualizar los datos de la impresora en el servicio de directorio.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Una estructura de la información de la [**impresora \_ \_ 8**](printer-info-8.md) que especifica la configuración de impresora predeterminada global.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 9**](printer-info-9.md) que especifica la configuración de impresora predeterminada por usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*Comando* \[ de\]
</dt> <dd>

la acción que se va a realizar.

Si el parámetro *LEVEL* es distinto de cero, establezca el valor de este parámetro en cero. En este caso, la impresora conserva su estado actual y la función vuelve a configurar los datos de la impresora según lo especificado por los parámetros *LEVEL* y *pPrinter* .

Si el parámetro *LEVEL* es cero, establezca el valor de este parámetro en uno de los siguientes valores.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**pausar control de impresora \_ \_**</dt> </dl>                 | Pausar la impresora.<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**\_purga de control de impresora \_**</dt> </dl>                 | Elimine todos los trabajos de impresión de la impresora.<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**\_reanudación del control de impresora \_**</dt> </dl>              | Reanudar una impresora en pausa.<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**\_Estado del \_ conjunto de control de impresora \_**</dt> </dl> | Establezca el estado de la impresora.<br/> Establezca el parámetro *pPrinter* en un puntero a un valor **DWORD** que especifique el nuevo estado de la impresora.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Si el *nivel* es 7 y se produce un error en la acción de publicación, **SetPrinter** devuelve un **error de \_ e/s \_ pendiente** e intenta completar la acción en segundo plano. Si el *nivel* es 7 y se produjo un error en la acción de actualización, **SetPrinter** devuelve el **archivo de error \_ \_ no \_ encontrado**.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

No se puede usar **SetPrinter** para cambiar la impresora predeterminada.

Para modificar la configuración actual de la impresora, llame a la función [**GetPrinter**](getprinter.md) para recuperar la configuración actual en una estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) , modifique los miembros de dicha estructura según sea necesario y, a continuación, llame a **SetPrinter**.

La función **SetPrinter** omite los miembros **pServerName**, **AveragePPM**, **status** y **CJobs** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) .

Al pausar una impresora, se suspende la programación de todos los trabajos de impresión de la impresora, excepto en el caso de los trabajos de impresión que se estén imprimiendo en ese momento. Los trabajos de impresión se pueden enviar a una impresora en pausa, pero no se programará ningún trabajo para imprimirlo en la impresora hasta que se reanude la impresión. Si una impresora está desactivada, se eliminarán todos los trabajos de impresión de la impresora, excepto el trabajo de impresión actual.

Si usa **SetPrinter** para modificar la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predeterminada de una impresora (estableciendo globalmente los valores predeterminados de la impresora), primero debe llamar a la función [**DocumentProperties**](documentproperties.md) para validar la estructura **DEVMODE** .

En el caso de las estructuras [**Printer \_ info \_ 2**](printer-info-2.md) y [**Printer \_ info \_ 3**](printer-info-3.md) que contienen un puntero a un descriptor de seguridad, la función solo puede establecer los componentes del descriptor de seguridad para los que el autor de la llamada tiene permiso de modificación. Para establecer determinados componentes de descriptor de seguridad, debe especificar los derechos de acceso necesarios cuando llame a la función [**OpenPrinter**](openprinter.md) o [**OpenPrinter2**](openprinter2.md) para recuperar un identificador de la impresora. En la tabla siguiente se muestran los derechos de acceso necesarios para modificar los distintos componentes del descriptor de seguridad.



| Permiso de acceso            | Componente de descriptor de seguridad             |
|------------------------------|-------------------------------------------|
| **propietario de escritura \_**             | Propietario<br/> Grupo primario<br/> |
| **ESCRIBIR \_ DAC**               | Lista de control de acceso discrecional (DACL)  |
| **ACCESO a la \_ seguridad del sistema \_** | Lista de control de acceso del sistema (SACL)         |



 

Si el descriptor de seguridad contiene un componente que el autor de la llamada no tiene el derecho de acceso para modificarlo, **SetPrinter** produce un error. Los componentes de un descriptor de seguridad que no desea modificar deberían ser **nulos** o no estar presentes, según corresponda. Si no desea modificar el descriptor de seguridad y está llamando a **SetPrinter** con una estructura de [**\_ información \_ 2**](printer-info-2.md) de la impresora, establezca el miembro **pSecurityDescriptor** de esa estructura en **null**.

El Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para compartir archivos e impresoras. Si un administrador del equipo llama a **SetPrinter** , habilita la excepción. Si lo llama un usuario que no es administrador y la excepción aún no se ha habilitado, se produce un error en la llamada.

Puede usar el nivel 7 con la estructura de la [**información de impresora \_ \_ 7**](printer-info-7.md) para publicar, anular la publicación o actualizar los datos del servicio de directorio para la impresora. Los datos del servicio de directorio para una impresora incluyen todos los datos almacenados en las claves de SPLDS \_ \* mediante llamadas a la función [**SetPrinterDataEx**](setprinterdataex.md) para la impresora. Antes de llamar a **SetPrinter**, establezca el miembro **pszObjectGUID** de la información de la **impresora \_ \_ 7** en **null** y establezca el miembro *dwAction* en uno de los siguientes valores.



| Value                             | Descripción                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **publicación de DSPRINT \_**<br/>   | Publica los datos del servicio de directorio.<br/>                                                                                                                                                                                                                                                                                                                                        |
| **DSPRINT \_ volver a publicar**<br/> | Los datos del servicio de directorio de la impresora no se publican y se vuelven a publicar, actualizando todas las propiedades de la impresora publicada. Al volver a publicar también se cambia el GUID de la impresora publicada. Use este valor si sospecha que los datos publicados de la impresora están dañados.<br/>                                                                                         |
| **DSPRINT \_ Anular publicación**<br/> | Anula la publicación de los datos del servicio de directorio.<br/>                                                                                                                                                                                                                                                                                                                                      |
| **actualización de DSPRINT \_**<br/>    | Actualiza los datos del servicio de directorio. Esto es lo mismo que **DSPRINT \_ PUBLISH**, salvo que se produce un error en **SetPrinter** con el **archivo de error \_ \_ no \_ encontrado** si la impresora no está publicada todavía.<br/> Use **la \_ actualización de DSPRINT** para actualizar las propiedades publicadas pero no forzar la publicación. Los controladores de impresora siempre deben usar **DSPRINT \_ Update** en lugar de **DSPRINT \_ PUBLISH**.<br/> |



 

**DSPRINT \_ PENDING** no es un valor *dwAction* válido para **SetPrinter**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>WinSpool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPrinterW** (Unicode) y **SetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Información de la impresora \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**Información de la impresora \_ \_ 6**](printer-info-6.md)
</dt> <dt>

[**Información de la impresora \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**Información de la impresora \_ \_ 8**](printer-info-8.md)
</dt> <dt>

[**Información de la impresora \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




