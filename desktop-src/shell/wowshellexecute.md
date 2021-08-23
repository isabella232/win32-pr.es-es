---
description: Realiza una operación en un archivo especificado.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Función WOWShellExecute
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
ms.openlocfilehash: 4389c348a06b7c54dc899da8114eee09e740681f043084bb0c32ab9f7163772e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591835"
---
# <a name="wowshellexecute-function"></a>Función WOWShellExecute

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Realiza una operación en un archivo especificado. **WOWShellExecute** solo existe para su uso con la máquina virtual dos de Microsoft Windows NT (Ntvdm.exe), que permite que el sistema operativo de disco (DOS) y el software de 16 bits se ejecuten en un sistema Windows y que nadie más pueda usar. Use [**ShellExecute en**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) su lugar.

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

*hwnd* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana de propietario que se usa para mostrar una interfaz de usuario o mensajes de error. Este valor puede ser **NULL** si la operación no está asociada a una ventana.

</dd> <dt>

*lpOperation* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a una cadena terminada en **NULL,** a la que se hace referencia en este caso como verbo *,* que especifica la acción que se va a realizar. El conjunto de verbos disponibles depende del archivo o carpeta en particular. Por lo general, las acciones disponibles en el menú contextual de un objeto son verbos disponibles. Para obtener más información sobre los verbos y su disponibilidad, vea la sección *Verbos de objeto* de [Iniciar aplicaciones](launch.md). Consulte [Extensión de menús contextuales para](context.md) obtener más información sobre los menús contextuales. Normalmente se usan los verbos siguientes.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**Editar**


</dt> <dd>

Inicia un editor y abre el documento para su edición. Si *lpFile* no es un archivo de documento, se producirá un error en la función.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**Explorar**


</dt> <dd>

Explora la carpeta especificada por *lpFile*.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**Encontrar**


</dt> <dd>

Inicia una búsqueda a partir del directorio especificado.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**Abierto**


</dt> <dd>

Abre el archivo especificado por el *parámetro lpFile.* El archivo puede ser un archivo ejecutable, un archivo de documento o una carpeta.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**Impresión**


</dt> <dd>

Imprime el archivo de documento especificado por *lpFile*. Si *lpFile* no es un archivo de documento, se producirá un error en la función.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**Null**


</dt> <dd>

Para los sistemas anteriores a Windows 2000, se usa el verbo predeterminado si es válido y está disponible en el Registro. Si no es así, se usa el verbo "abrir".

Para Windows sistemas 2000 y posteriores, se usa el verbo predeterminado si está disponible. Si no es así, se usa el verbo "abrir". Si ninguno de los verbos está disponible, el sistema usa el primer verbo enumerado en el registro.

</dd> </dl> </dd> <dt>

*lpFile* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a una **cadena terminada** en NULL que especifica el archivo u objeto en el que se va a ejecutar el verbo especificado. Para especificar un objeto de espacio de nombres de Shell, pase el nombre completo del análisis. Tenga en cuenta que no todos los verbos se admiten en todos los objetos. Por ejemplo, no todos los tipos de documento admiten el verbo "print".

</dd> <dt>

*lpParameters* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Si el *parámetro lpFile* especifica un archivo ejecutable, *lpParameters* es un puntero a una cadena terminada en **NULL** que especifica los parámetros que se pasarán a la aplicación. El formato de esta cadena viene determinado por el verbo que se va a invocar. Si *lpFile* especifica un archivo de documento, *lpParameters* debe ser **NULL.**

</dd> <dt>

*lpDirectory* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a una **cadena terminada** en NULL que especifica el directorio predeterminado.

</dd> <dt>

*nShowCmd* \[ En\]
</dt> <dd>

Tipo: **INT**

Marcas que especifican cómo se mostrará una aplicación cuando se abra. Si *lpFile* especifica un archivo de documento, la marca simplemente se pasa a la aplicación asociada. Es decisión de la aplicación decidir cómo controlarla. Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la [función ShowWindow.](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Tipo: **\* void**

Función de devolución de llamada que se [**usa para llamar a CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en el kernel de 16 bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HINSTANCE**

Devuelve un valor mayor que 32 si se realiza correctamente o un valor de error menor o igual que 32 en caso contrario. En la tabla siguiente se enumeran los valores de error. El valor devuelto se convierte como HINSTANCE para la compatibilidad con versiones anteriores con aplicaciones de Windows de 16 bits. Sin embargo, no es un HINSTANCE verdadero. Lo único que se puede hacer con la instancia HINSTANCE devuelta es convertirla a un **valor int** y compararlo con el valor 32 o uno de los códigos de error siguientes.



| Código devuelto                                                                                             | Descripción                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | El sistema operativo está sin memoria o recursos.<br/>                                                                                                           |
| <dl> <dt>**ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO**</dt> </dl>  | No se encontró el archivo especificado.<br/>                                                                                                                             |
| <dl> <dt>**RUTA DE \_ ACCESO DE ERROR NO \_ \_ ENCONTRADA**</dt> </dl>  | No se encontró la ruta de acceso especificada.<br/>                                                                                                                             |
| <dl> <dt>**FORMATO \_ DE ERROR NO \_ CORRECTO**</dt> </dl>       | El .exe no es válido (no es .exe win32 o error en .exe imagen).<br/>                                                                                             |
| <dl> <dt>**\_SE ACCESO \_ DE ERRORDENIED**</dt> </dl>    | El sistema operativo denegó el acceso al archivo especificado.<br/>                                                                                                     |
| <dl> <dt>**\_SE ERR \_ ASSOCINCOMPLETE**</dt> </dl> | La asociación de nombre de archivo está incompleta o no es válida.<br/>                                                                                                           |
| <dl> <dt>**\_SE ERR \_ DDEBUSY**</dt> </dl>         | No se pudo completar la transacción DDE porque se estaban procesando otras transacciones DDE.<br/>                                                               |
| <dl> <dt>**\_SE ERR \_ DDEFAIL**</dt> </dl>         | Error en la transacción DDE.<br/>                                                                                                                                   |
| <dl> <dt>**\_SE ERR \_ DDETIMEOUT**</dt> </dl>      | No se pudo completar la transacción DDE porque la solicitud ha finalizado el tiempo de espera.<br/>                                                                                     |
| <dl> <dt>**\_SE ERR \_ DLLNOTFOUND**</dt> </dl>     | No se encontró el archivo DLL especificado.<br/>                                                                                                                              |
| <dl> <dt>**\_SE ERR \_ FNF**</dt> </dl>             | No se encontró el archivo especificado.<br/>                                                                                                                             |
| <dl> <dt>**\_SE ERR \_ NOASSOC**</dt> </dl>         | No hay ninguna aplicación asociada a la extensión de nombre de archivo dada. Este error también se devolverá si intenta imprimir un archivo que no es imprimible.<br/> |
| <dl> <dt>**\_SE ERR \_ OOM**</dt> </dl>             | No había suficiente memoria para completar la operación.<br/>                                                                                                        |
| <dl> <dt>**\_SE ERR \_ PNF**</dt> </dl>             | No se encontró la ruta de acceso especificada.<br/>                                                                                                                             |
| <dl> <dt>**\_SE RECURSO \_ COMPARTIDO DE ERR**</dt> </dl>           | Se ha producido una infracción de uso compartido.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

**WOWShellExecute** no se incluye en un archivo de encabezado o .lib. Se exporta desde Shell32.dll por nombre.

Este método permite ejecutar cualquier comando en el menú contextual de una carpeta o almacenarse en el Registro.

Si *lpOperation* es **NULL,** la función abre el archivo especificado por *lpFile*. Si *lpOperation* es "open" o "explore", la función intenta abrir o explorar la carpeta.

Para obtener información sobre la aplicación que se inicia como resultado de llamar a **WOWShellExecute,** use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> La **opción Iniciar ventanas de carpeta en un proceso** independiente en Opciones de carpeta afecta a **WOWShellExecute.** Si esa opción está deshabilitada (la configuración predeterminada), **WOWShellExecute** usa una ventana del Explorador abierta en lugar de iniciar una nueva. Si no hay ninguna ventana del Explorador abierta, **WOWShellExecute** inicia una nueva.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
