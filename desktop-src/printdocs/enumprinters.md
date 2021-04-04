---
description: La función EnumPrinters enumera las impresoras, los servidores de impresión, los dominios o los proveedores de impresión disponibles.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Función EnumPrinters (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909589"
---
# <a name="enumprinters-function"></a>EnumPrinters función)

La función **EnumPrinters** enumera las impresoras, los servidores de impresión, los dominios o los proveedores de impresión disponibles.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Los tipos de objetos de impresión que la función debe enumerar. Este valor puede ser uno o varios de los siguientes valores.



| Value                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**\_enumeración \_ local de impresora**</dt> </dl>                       | Si \_ \_ no se pasa también la marca Printer enum Name, la función omite el parámetro *Name* y enumera las impresoras instaladas localmente. Si \_ también se pasa el nombre de la enumeración de impresora \_ , la función enumera las impresoras locales en el *nombre*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**nombre de la \_ enumeración de impresora \_**</dt> </dl>                          | La función enumera la impresora identificada por el *nombre*. Puede ser un servidor, un dominio o un proveedor de impresión. Si *Name* es **null**, la función enumera los proveedores de impresión disponibles.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**\_enumeración de impresora \_ compartida**</dt> </dl>                    | La función enumera las impresoras que tienen el atributo Shared. No se puede usar en aislamiento; Use una operación o para combinar con otro \_ tipo de enumeración de impresora.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**\_conexiones de enumeración de impresora \_**</dt> </dl>     | La función enumera la lista de impresoras en las que el usuario ha realizado conexiones anteriores.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**\_red enum de impresora \_**</dt> </dl>                 | La función enumera las impresoras de red en el dominio del equipo. Este valor solo es válido si el *nivel* es 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**\_enumeración de impresora \_ remota**</dt> </dl>                    | La función enumera las impresoras de red y los servidores de impresión en el dominio del equipo. Este valor solo es válido si el *nivel* es 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**\_Categoría de enumeración de impresora \_ \_ 3D**</dt> </dl>    | La función solo enumera las impresoras 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**Categoría de enum de impresora \_ \_ \_ All**</dt> </dl> | La función enumera todos los dispositivos de impresión, incluidas las impresoras 3D.<br/>                                                                                                                                                                           |



 

Si el *nivel* es 4, solo puede usar las constantes de enumeración Printer \_ \_ Connection y Printer \_ enum \_ local.

> [!Note]  
> los dispositivos de impresión 3D no se enumeran de forma predeterminada. Debe incluir la **categoría de \_ enum \_ Printer \_ 3D** y **Printer \_ enum \_ local** para enumerar solo las impresoras 3D. Para incluir impresoras 3D, junto con todas las demás impresoras locales, use **Printer \_ enum \_ Category \_ All** y **Printer \_ enum \_ local**.

 

</dd> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Si el *nivel* es 1, las *marcas* contienen \_ el nombre de la enumeración de la impresora \_ y *el nombre* no es **null**, el *nombre* es un puntero a una cadena terminada en null que especifica el nombre del objeto que se va a enumerar. Esta cadena puede ser el nombre de un servidor, un dominio o un proveedor de impresión.

Si el *nivel* es 1, las *marcas* contienen el nombre de la enumeración de la impresora \_ y el \_ *nombre* es **null**, la función enumera los proveedores de impresión disponibles.

Si *LEVEL* es 1, *Flags* contiene Printer \_ enum \_ Remote y *Name* es **null**, la función enumera las impresoras del dominio del usuario.

Si *LEVEL* es 2 o 5,*Name* es un puntero a una cadena terminada en null que especifica el nombre de un servidor cuyas impresoras se van a enumerar. Si esta cadena es **null**, la función enumera las impresoras instaladas en el equipo local.

Si el *nivel* es 4, *el nombre* debe ser **null**. La función siempre realiza consultas en el equipo local.

Cuando *el* valor de Name es **null**, al establecer *Flags* en Printer \_ enum \_ local \| Printer \_ enum \_ Connections se enumeran las impresoras instaladas en el equipo local. Estas impresoras incluyen las que están conectadas físicamente al equipo local, así como a las impresoras remotas en las que tiene una conexión de red.

Cuando *Name* no es **null**, al establecer *Flags* en Printer \_ enum \_ local \| Printer \_ \_ Name enum se enumeran las impresoras locales instaladas en el *nombre* del servidor.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Tipo de estructuras de datos a las que apunta *pPrinterEnum*. Los valores válidos son 1, 2, 4 y 5, que corresponden a las estructuras de datos de la información de la [**impresora \_ \_ 1**](printer-info-1.md), la información de la [**impresora \_ \_ 2**](printer-info-2.md) , la información de la [**impresora \_ \_ 4**](printer-info-4.md)y la información de la [**impresora \_ \_ 5**](printer-info-5.md) .

Este valor puede ser 1, 2, 4 o 5.

</dd> <dt>

*pPrinterEnum* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe una matriz de las estructuras de la información de la [**impresora \_ \_ 1**](printer-info-1.md), la información de la impresora [**\_ \_ 2**](printer-info-2.md), la información de la [**impresora \_ \_ 4**](printer-info-4.md)o la información de la [**impresora \_ \_ 5**](printer-info-5.md) . Cada estructura contiene datos que describen un objeto de impresión disponible.

Si el *nivel* es 1, la matriz contiene estructuras de [**información de impresora \_ \_ 1**](printer-info-1.md) . Si el *nivel* es 2, la matriz contiene estructuras de [**\_ información \_ 2**](printer-info-2.md) de la impresora. Si el *nivel* es 4, la matriz contiene estructuras de la información de la [**impresora \_ \_ 4**](printer-info-4.md) . Si el *nivel* es 5, la matriz contiene estructuras de [**\_ información \_ 5**](printer-info-5.md) de la impresora.

El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras de datos y las cadenas u otros datos a los que apuntan los miembros de la estructura. Si el búfer es demasiado pequeño, el parámetro *pcbNeeded* devuelve el tamaño de búfer necesario.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pPrinterEnum*.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> <dt>

*pcReturned* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que recibe el número de estructuras de la información de la [**impresora \_ \_ 1**](printer-info-1.md), la información de la [**impresora \_ \_ 2**](printer-info-2.md) , la información de la [**impresora \_ \_ 4**](printer-info-4.md)o las estructuras de la información de la impresora [**\_ \_ 5**](printer-info-5.md) que devuelve la función en la matriz a la que señala *pPrinterEnum* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Si **EnumPrinters** devuelve una estructura de [**información de impresora \_ \_ 1**](printer-info-1.md) en la que \_ se especifica el contenedor de enumeración de impresora \_ , esto indica que hay una jerarquía de objetos de impresora. Una aplicación puede enumerar la jerarquía llamando a **EnumPrinters** de nuevo, estableciendo el *nombre* en el valor del miembro **pName** de la estructura de **\_ información \_** de la impresora.

La función **EnumPrinters** no recupera información de seguridad. Si se devuelven las estructuras de la información de la [**impresora \_ \_ 2**](printer-info-2.md) en la matriz a la que señala *pPrinterEnum*, sus miembros *pSecurityDescriptor* se establecerán en **null**.

Para obtener información acerca de la impresora predeterminada, llame a [**GetDefaultPrinter**](getdefaultprinter.md).

La estructura de la información de la [**impresora \_ \_ 4**](printer-info-4.md) proporciona una manera fácil y sumamente rápida de recuperar los nombres de las impresoras instaladas en un equipo local, así como las conexiones remotas que ha establecido un usuario. Cuando se llama a **EnumPrinters** con una estructura de datos de la información de la **impresora \_ \_ 4** , esa función consulta el registro para obtener la información especificada y, a continuación, vuelve inmediatamente. Esto difiere del comportamiento de **EnumPrinters** cuando se llama con otros niveles de **información de impresora \_ \_ \* *_ estructuras de datos. En concreto, cuando*** se llama a _ EnumPrinters con una estructura de datos de nivel 2 (información de la [**impresora \_ \_ 2**](printer-info-2.md)), realiza una llamada [**OpenPrinter**](openprinter.md) en cada conexión remota. Si una conexión remota está inactiva o el servidor remoto ya no existe o la impresora remota ya no existe, la función debe esperar a que se agote el tiempo de espera de RPC y, por tanto, se produzca un error en la llamada **OpenPrinter** . Esto puede tardar unos minutos. Pasar una estructura de la información de la **impresora \_ \_ 4** permite que una aplicación recupere un mínimo de la información necesaria; si se desea obtener información más detallada, se puede realizar una llamada posterior al nivel 2 de **EnumPrinters** .

**Windows Vista:** Los datos de la impresora devueltos por **EnumPrinters** se recuperan de una caché local cuando el valor del *nivel* es 4.

En la tabla siguiente se muestra la salida de **EnumPrinters** para varios valores de *marcas* cuando el parámetro *LEVEL* está establecido en 1.

En la columna parámetro de *nombre* de la tabla, debe sustituir un nombre apropiado para el proveedor de impresión, el dominio y la máquina. Por ejemplo, para "proveedor de impresión", puede usar el nombre del proveedor de impresión de red o el nombre del proveedor de impresión local. Para recuperar los nombres de proveedor de impresión, llame a **EnumPrinters** con *el nombre* establecido en **null**.



| *Flags* , parámetro                                  | Parámetro *Name*                            | Resultado                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| \_Enumeración \_ de impresora local (y no \_ nombre de enumeración de impresora \_ ) | Se omite el parámetro *Name* .<br/> | Todas las impresoras locales.<br/>                                                                    |
| nombre de la \_ enumeración de impresora \_                                | "Proveedor de impresión"<br/>                 | Todos los nombres de dominio<br/>                                                                       |
| nombre de la \_ enumeración de impresora \_                                | "Proveedor de impresión! Dominio<br/>          | Todas las impresoras y servidores de impresión en el dominio del equipo<br/>                                |
| nombre de la \_ enumeración de impresora \_                                | "Print Provider!! \\ \\ Sistema<br/>    | Todas las impresoras compartidas en el \\ \\ equipo<br/>                                                     |
| nombre de la \_ enumeración de impresora \_                                | Una cadena vacía, ""<br/>              | Todas las impresoras locales.<br/>                                                                    |
| nombre de la \_ enumeración de impresora \_                                | **NULL**<br/>                         | Todos los proveedores de impresión en el dominio del equipo<br/>                                           |
| \_conexiones de enumeración de impresora \_                         | Se omite el parámetro *Name* .<br/> | Todas las impresoras remotas conectadas<br/>                                                          |
| \_red enum de impresora \_                             | Se omite el parámetro *Name* .<br/> | Todas las impresoras del dominio del equipo<br/>                                                  |
| \_enumeración de impresora \_ remota                              | Una cadena vacía, ""<br/>              | Todas las impresoras y servidores de impresión en el dominio del equipo<br/>                                |
| \_enumeración de impresora \_ remota                              | "Proveedor de impresión"<br/>                 | Igual que \_ el nombre de la enumeración de impresora \_<br/>                                                            |
| \_enumeración de impresora \_ remota                              | "Proveedor de impresión! Dominio<br/>          | Todas las impresoras y servidores de impresión del dominio del equipo, independientemente del *dominio* especificado.<br/> |
| \_Categoría de enumeración de impresora \_ \_ 3D                        | Se omite el parámetro *Name* .<br/> | Solo se enumeran las impresoras 3D.<br/>                                                       |
| Categoría de enum de impresora \_ \_ \_ All                       | Se omite el parámetro *Name* .<br/> | las impresoras 3D se enumeran, junto con todas las demás impresoras.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrintersW** (Unicode) y **EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Información de la impresora \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

