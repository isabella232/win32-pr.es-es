---
description: La función EnumPrinters enumera las impresoras, servidores de impresión, dominios o proveedores de impresión disponibles.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Función EnumPrinters (Winspool.h)
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
ms.openlocfilehash: fb88cef081010f1319fb194904933ba2366d6593f0d2517c696bb6d6490ace20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353845"
---
# <a name="enumprinters-function"></a>Función EnumPrinters

La **función EnumPrinters** enumera las impresoras, servidores de impresión, dominios o proveedores de impresión disponibles.

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

*Marcas* \[ En\]
</dt> <dd>

Tipos de objetos de impresión que la función debe enumerar. Este valor puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**ENUMERACIÓN \_ DE IMPRESORA \_ LOCAL**</dt> </dl>                       | Si no se pasa también la marca PRINTER ENUM NAME, la función omite el parámetro Name y enumera las \_ \_ impresoras instaladas localmente.  Si también \_ se pasa PRINTER ENUM NAME, la función enumera las \_ impresoras locales en *Name*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**NOMBRE \_ DE ENUMERACIÓN DE \_ IMPRESORA**</dt> </dl>                          | La función enumera la impresora identificada por *Name*. Puede ser un servidor, un dominio o un proveedor de impresión. Si *Name* es **NULL,** la función enumera los proveedores de impresión disponibles.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**ENUMERACIÓN \_ DE IMPRESORA \_ COMPARTIDA**</dt> </dl>                    | La función enumera las impresoras que tienen el atributo compartido. No se puede usar de forma aislada; use una operación OR para combinar con otro tipo PRINTER \_ ENUM.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**CONEXIONES \_ DE ENUMERACIÓN DE \_ IMPRESORA**</dt> </dl>     | La función enumera la lista de impresoras a las que el usuario ha realizado conexiones anteriores.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**RED \_ DE ENUMERACIÓN DE \_ IMPRESORA**</dt> </dl>                 | La función enumera las impresoras de red en el dominio del equipo. Este valor solo es válido si *Level* es 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**ENUMERACIÓN \_ DE IMPRESORA \_ REMOTA**</dt> </dl>                    | La función enumera las impresoras de red y los servidores de impresión en el dominio del equipo. Este valor solo es válido si *Level* es 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**CATEGORÍA \_ \_ 3D DE ENUMERACIÓN \_ DE IMPRESORA**</dt> </dl>    | La función enumera solo impresoras 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**CATEGORÍA \_ DE \_ ENUMERACIÓN DE IMPRESORA \_ TODO**</dt> </dl> | La función enumera todos los dispositivos de impresión, incluidas las impresoras 3D.<br/>                                                                                                                                                                           |



 

Si *Level* es 4, solo puede usar las constantes PRINTER ENUM CONNECTIONS e \_ PRINTER \_ \_ ENUM \_ LOCAL.

> [!Note]  
> Los dispositivos de impresión 3D no se enumeran de forma predeterminada. Debe incluir PRINTER **\_ ENUM \_ CATEGORY \_ 3D** e **PRINTER \_ ENUM \_ LOCAL** para enumerar solo impresoras 3D. Para incluir impresoras 3D, junto con todas las demás impresoras locales, use **PRINTER \_ ENUM \_ CATEGORY \_ ALL** e **PRINTER \_ ENUM \_ LOCAL**.

 

</dd> <dt>

*Nombre* \[ En\]
</dt> <dd>

Si *Level* es 1, *Flags* contiene PRINTER ENUM NAME y Name es distinto de NULL, name es un puntero a una cadena terminada en NULL que especifica el nombre del objeto que se va \_ a \_ enumerar.    Esta cadena puede ser el nombre de un servidor, un dominio o un proveedor de impresión.

Si *Level* es 1, *Flags* contiene PRINTER ENUM NAME y Name es NULL, la función \_ enumera los proveedores de impresión \_ disponibles.  

Si *Level* es 1, *Flags* contiene PRINTER ENUM REMOTE y Name es NULL, la función enumera las impresoras en el \_ dominio del \_ usuario.  

Si *Level* es 2 o 5,*Name* es un puntero a una cadena terminada en NULL que especifica el nombre de un servidor cuyas impresoras se van a enumerar. Si esta cadena es **NULL,** la función enumera las impresoras instaladas en el equipo local.

Si *Level* es 4, *El nombre* debe ser **NULL.** La función siempre consulta en el equipo local.

Cuando *Name* es **NULL,** al establecer *Flags* en PRINTER ENUM LOCAL PRINTER ENUM CONNECTIONS se enumeran las impresoras que están \_ instaladas en el equipo \_ \| \_ \_ local. Estas impresoras incluyen las que están conectadas físicamente a la máquina local, así como las impresoras remotas a las que tiene una conexión de red.

Si *Name* no es **NULL,** al establecer *Flags* en PRINTER ENUM LOCAL PRINTER ENUM NAME se enumeran las \_ \_ \| \_ impresoras \_ locales que están instaladas en el nombre del servidor .

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de estructuras de datos a las que apunta *pPrinterEnum.* Los valores válidos son 1, 2, 4 y 5, que corresponden a las estructuras de datos [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)e [**PRINTER INFO \_ \_ 5.**](printer-info-5.md)

Este valor puede ser 1, 2, 4 o 5.

</dd> <dt>

*pPrinterEnum* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)o [**PRINTER INFO \_ \_ 5.**](printer-info-5.md) Cada estructura contiene datos que describen un objeto de impresión disponible.

Si *Level* es 1, la matriz contiene [**estructuras PRINTER INFO \_ \_ 1.**](printer-info-1.md) Si *Level* es 2, la matriz contiene [**estructuras PRINTER INFO \_ \_ 2.**](printer-info-2.md) Si *Level* es 4, la matriz contiene [**estructuras PRINTER INFO \_ \_ 4.**](printer-info-4.md) Si *Level* es 5, la matriz contiene [**estructuras PRINTER INFO \_ \_ 5.**](printer-info-5.md)

El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras de datos y las cadenas u otros datos a los que apuntan los miembros de la estructura. Si el búfer es demasiado pequeño, el *parámetro fueneeded* devuelve el tamaño de búfer necesario.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pPrinterEnum*.

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a un valor que recibe el número de bytes copiados si la función se realiza correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a un valor que recibe el número de estructuras [**PRINTER \_ INFO \_ 1**](printer-info-1.md), [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)o [**PRINTER INFO \_ \_ 5**](printer-info-5.md) que la función devuelve en la matriz a la que *apunta pPrinterEnum.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Si **EnumPrinters** devuelve una estructura [**PRINTER INFO \_ \_ 1**](printer-info-1.md) en la que se especifica PRINTER ENUM CONTAINER, esto indica que hay una \_ jerarquía de objetos de \_ impresora. Una aplicación puede enumerar la jerarquía llamando de nuevo **a EnumPrinters,** estableciendo *Name* en el valor del miembro **pName** de la estructura **PRINTER INFO \_ \_ 1.**

La **función EnumPrinters** no recupera información de seguridad. Si se devuelven estructuras [**PRINTER INFO \_ \_ 2**](printer-info-2.md) en la matriz a la que apunta *pPrinterEnum*, sus *miembros pSecurityDescriptor* se establecerán en **NULL.**

Para obtener información sobre la impresora predeterminada, llame a [**GetDefaultPrinter**](getdefaultprinter.md).

La [**estructura PRINTER INFO \_ \_ 4**](printer-info-4.md) proporciona una manera fácil y muy rápida de recuperar los nombres de las impresoras instaladas en un equipo local, así como las conexiones remotas que un usuario ha establecido. Cuando se llama a **EnumPrinters** con una estructura de datos **PRINTER INFO \_ \_ 4,** esa función consulta al Registro para obtener la información especificada y, a continuación, devuelve inmediatamente. Esto difiere del comportamiento de **EnumPrinters** cuando se llama con otros niveles de estructuras de datos **PRINTER INFO \_ \_ \* *_. En concreto, cuando se*** llama a _ EnumPrinters con una estructura de datos de nivel [**2 (PRINTER \_ INFO \_ 2),**](printer-info-2.md)realiza una llamada a [**OpenPrinter**](openprinter.md) en cada conexión remota. Si una conexión remota está fuera de servicio, o el servidor remoto ya no existe, o la impresora remota ya no existe, la función debe esperar a que RPC se aleme del tiempo de espera y, por tanto, se producirá un error en la llamada a **OpenPrinter.** Esto puede tardar unos minutos. Pasar una **estructura PRINTER \_ INFO \_ 4** permite a una aplicación recuperar un mínimo de la información necesaria; si se desea información más detallada, se puede realizar una llamada posterior **a EnumPrinters** de nivel 2.

**Windows Vista:** Los datos de impresora devueltos por **EnumPrinters** se recuperan de una caché local cuando el valor de *Level* es 4.

En la tabla siguiente se muestra **la salida de EnumPrinters** para varios *valores flags* cuando el *parámetro Level* está establecido en 1.

En la *columna parámetro* Name de la tabla, debe sustituir un nombre adecuado por Proveedor de impresión, Dominio y Máquina. Por ejemplo, para "Proveedor de impresión", podría usar el nombre del proveedor de impresión de red o el nombre del proveedor de impresión local. Para recuperar nombres de proveedor de impresión, llame **a EnumPrinters** con *El nombre* establecido en **NULL.**



| *Parámetro Flags*                                  | *Parámetro name*                            | Resultado                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| PRINTER \_ ENUM \_ LOCAL (y no PRINTER \_ ENUM \_ NAME) | Se *omite* el parámetro Name.<br/> | Todas las impresoras locales.<br/>                                                                    |
| NOMBRE \_ DE ENUMERACIÓN DE \_ IMPRESORA                                | "Proveedor de impresión"<br/>                 | Todos los nombres de dominio<br/>                                                                       |
| NOMBRE \_ DE ENUMERACIÓN DE \_ IMPRESORA                                | "Proveedor de impresión. Dominio"<br/>          | Todas las impresoras y servidores de impresión del dominio del equipo<br/>                                |
| NOMBRE \_ DE ENUMERACIÓN DE \_ IMPRESORA                                | "Proveedor de impresión!" \\ \\ Máquina"<br/>    | Todas las impresoras compartidas en \\ \\ la máquina<br/>                                                     |
| NOMBRE \_ DE ENUMERACIÓN DE \_ IMPRESORA                                | Una cadena vacía, ""<br/>              | Todas las impresoras locales.<br/>                                                                    |
| NOMBRE \_ DE ENUMERACIÓN DE \_ IMPRESORA                                | **NULL**<br/>                         | Todos los proveedores de impresión del dominio del equipo<br/>                                           |
| CONEXIONES \_ DE ENUMERACIÓN DE \_ IMPRESORA                         | Se *omite* el parámetro Name.<br/> | Todas las impresoras remotas conectadas<br/>                                                          |
| RED \_ DE ENUMERACIÓN DE \_ IMPRESORA                             | Se *omite* el parámetro Name.<br/> | Todas las impresoras del dominio del equipo<br/>                                                  |
| PRINTER \_ ENUM \_ REMOTE                              | Una cadena vacía, ""<br/>              | Todas las impresoras y servidores de impresión del dominio del equipo<br/>                                |
| PRINTER \_ ENUM \_ REMOTE                              | "Proveedor de impresión"<br/>                 | Igual que PRINTER \_ ENUM \_ NAME<br/>                                                            |
| PRINTER \_ ENUM \_ REMOTE                              | "Proveedor de impresión. Dominio"<br/>          | Todas las impresoras y servidores de impresión del dominio del equipo, independientemente del *dominio* especificado.<br/> |
| CATEGORÍA \_ \_ 3D DE ENUMERACIÓN DE \_ IMPRESORA                        | Se *omite* el parámetro Name.<br/> | Solo se enumeran las impresoras 3D.<br/>                                                       |
| CATEGORÍA \_ DE ENUMERACIÓN \_ DE IMPRESORA \_ TODO                       | Se *omite* el parámetro Name.<br/> | Se enumeran las impresoras 3D, junto con todas las demás impresoras.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrintersW** (Unicode) y **EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 1**](printer-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

