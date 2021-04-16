---
description: Realiza una operación en un archivo especificado.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187806"
---
# <a name="wowshellexecute-function"></a>WOWShellExecute función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Realiza una operación en un archivo especificado. **WOWShellExecute** solo existe para su uso con la máquina virtual dos de Microsoft Windows NT (Ntvdm.exe), que permite que el sistema operativo de disco (dos) y el software de 16 bits se ejecuten en un sistema de Windows y no debe usarlos nadie más. En su lugar, use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="syntax"></a>Sintaxis


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana propietaria que se usa para mostrar una interfaz de usuario o mensajes de error. Este valor puede ser **null** si la operación no está asociada a una ventana.

</dd> <dt>

*lpOperation* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a una cadena terminada en **null**, a la que se hace referencia en este caso como *verbo*, que especifica la acción que se va a realizar. El conjunto de verbos disponibles depende del archivo o la carpeta determinados. Por lo general, las acciones disponibles en el menú contextual de un objeto son verbos disponibles. Para obtener más información sobre los verbos y su disponibilidad, vea la sección *verbos de objetos* de [Launching Applications](launch.md). Vea [extender menús contextuales](context.md) para obtener más información sobre los menús contextuales. Normalmente se utilizan los siguientes verbos.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**editar**


</dt> <dd>

Inicia un editor y abre el documento para su edición. Si *lpFile* no es un archivo de documento, se producirá un error en la función.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**visite**


</dt> <dd>

Explora la carpeta especificada por *lpFile*.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**localización**


</dt> <dd>

Inicia una búsqueda a partir del directorio especificado.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**Ábra**


</dt> <dd>

Abre el archivo especificado por el parámetro *lpFile* . El archivo puede ser un archivo ejecutable, un archivo de documento o una carpeta.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**imprime**


</dt> <dd>

Imprime el archivo de documento especificado por *lpFile*. Si *lpFile* no es un archivo de documento, se producirá un error en la función.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**ACEPTA**


</dt> <dd>

En sistemas anteriores a Windows 2000, se utiliza el verbo predeterminado si es válido y está disponible en el registro. Si no es así, se utiliza el verbo "abrir".

En el caso de los sistemas Windows 2000 y versiones posteriores, se utiliza el verbo predeterminado si está disponible. Si no es así, se utiliza el verbo "abrir". Si no hay ningún verbo disponible, el sistema utiliza el primer verbo enumerado en el registro.

</dd> </dl> </dd> <dt>

*lpFile* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a una cadena terminada en **null** que especifica el archivo o el objeto en el que se va a ejecutar el verbo especificado. Para especificar un objeto de espacio de nombres de Shell, pase el nombre de análisis completo. Tenga en cuenta que no todos los verbos se admiten en todos los objetos. Por ejemplo, no todos los tipos de documentos admiten el verbo "Imprimir".

</dd> <dt>

*lpParameters* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Si el parámetro *lpFile* especifica un archivo ejecutable, *lpParameters* es un puntero a una cadena terminada en **null** que especifica los parámetros que se van a pasar a la aplicación. El formato de esta cadena viene determinado por el verbo que se va a invocar. Si *lpFile* especifica un archivo de documento, *LpParameters* debe ser **null**.

</dd> <dt>

*lpDirectory* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a una cadena terminada en **null** que especifica el directorio predeterminado.

</dd> <dt>

*nShowCmd* \[ de\]
</dt> <dd>

Tipo: **int**

Marcas que especifican cómo se va a mostrar una aplicación cuando se abre. Si *lpFile* especifica un archivo de documento, la marca simplemente se pasa a la aplicación asociada. Depende de la aplicación decidir cómo controlarla. Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la función [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Tipo: **void \***

Función de devolución de llamada que se usa para llamar a [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en el kernel de 16 bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **hInstance**

Devuelve un valor mayor que 32 si es correcto, o un valor de error menor o igual que 32 en caso contrario. En la tabla siguiente se enumeran los valores de error. El valor devuelto se convierte en un HINSTANCE para la compatibilidad con versiones anteriores de aplicaciones Windows de 16 bits. Sin embargo, no es un HINSTANCE verdadero. Lo único que se puede hacer con el HINSTANCE devuelto es convertirlo en un **int** y compararlo con el valor 32 o con uno de los códigos de error siguientes.



| Código devuelto                                                                                             | Descripción                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | El sistema operativo no tiene memoria o recursos.<br/>                                                                                                           |
| <dl> <dt>**\_ \_ no \_ se encontró el archivo de error**</dt> </dl>  | No se encontró el archivo especificado.<br/>                                                                                                                             |
| <dl> <dt>**\_ \_ no \_ se encontró la ruta de error**</dt> </dl>  | No se encontró la ruta de acceso especificada.<br/>                                                                                                                             |
| <dl> <dt>**ERROR \_ de \_ formato incorrecto**</dt> </dl>       | El archivo. exe no es válido (no es Win32. exe o error en la imagen. exe).<br/>                                                                                             |
| <dl> <dt>**\_error de \_ ACCESSDENIED**</dt> </dl>    | El sistema operativo denegó el acceso al archivo especificado.<br/>                                                                                                     |
| <dl> <dt>**\_error de \_ ASSOCINCOMPLETE**</dt> </dl> | La Asociación de nombre de archivo está incompleta o no es válida.<br/>                                                                                                           |
| <dl> <dt>**\_error de \_ DDEBUSY**</dt> </dl>         | No se pudo completar la transacción DDE porque se estaban procesando otras transacciones DDE.<br/>                                                               |
| <dl> <dt>**\_error de \_ DDEFAIL**</dt> </dl>         | Error en la transacción DDE.<br/>                                                                                                                                   |
| <dl> <dt>**\_error de \_ DDETIMEOUT**</dt> </dl>      | No se pudo completar la transacción DDE porque se agotó el tiempo de espera de la solicitud.<br/>                                                                                     |
| <dl> <dt>**\_error de \_ DLLNOTFOUND**</dt> </dl>     | No se encontró la DLL especificada.<br/>                                                                                                                              |
| <dl> <dt>**\_error de \_ FNF**</dt> </dl>             | No se encontró el archivo especificado.<br/>                                                                                                                             |
| <dl> <dt>**SE ha $ \_ \_ Assoc**</dt> </dl>         | No hay ninguna aplicación asociada a la extensión de nombre de archivo especificada. También se devolverá este error si intenta imprimir un archivo que no se puede imprimir.<br/> |
| <dl> <dt>**\_error de \_ OOM**</dt> </dl>             | No había memoria suficiente para completar la operación.<br/>                                                                                                        |
| <dl> <dt>**SE \_ Err error \_ PNF**</dt> </dl>             | No se encontró la ruta de acceso especificada.<br/>                                                                                                                             |
| <dl> <dt>**\_recurso compartido de error se \_**</dt> </dl>           | Se ha producido una infracción de uso compartido.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

**WOWShellExecute** no se incluye en un archivo de encabezado o. lib. Se exporta desde Shell32.dll por nombre.

Este método permite ejecutar cualquier comando en el menú contextual de una carpeta o almacenarlo en el registro.

Si *lpOperation* es **null**, la función abre el archivo especificado por *lpFile*. Si *lpOperation* es "Open" o "Explore", la función intenta abrir o explorar la carpeta.

Para obtener información sobre la aplicación que se inicia como resultado de llamar a **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> Las **ventanas de la carpeta de inicio en una configuración de proceso independiente** en opciones de carpeta afectan a **WOWShellExecute**. Si esa opción está deshabilitada (la configuración predeterminada), **WOWShellExecute** usa una ventana de explorador abierta en lugar de iniciar una nueva. Si no hay ninguna ventana del explorador abierta, **WOWShellExecute** inicia una nueva.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
