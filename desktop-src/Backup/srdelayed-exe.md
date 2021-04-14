---
title: Srdelayed.exe
description: Es posible que las aplicaciones que realizan operaciones de restauración de estado del sistema al principio del sistema operativo no puedan usar las funciones de administración de archivos para quitar, eliminar o establecer el nombre corto de determinados archivos del sistema.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Copia de seguridad de Srdelayed.exe
- Copia de seguridad de recuperación de estado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5f6b281c07f5b0ad8d6cd7e59b4f93ec9208a5
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104488459"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Es posible que las aplicaciones que realizan operaciones de restauración de estado del sistema al principio del sistema operativo no puedan usar las funciones de administración de archivos para quitar, eliminar o establecer el nombre corto de determinados archivos del sistema. Srdelayed.exe es un archivo ejecutable, proporcionado con la característica Copias de seguridad de Windows Server (WSB) en Windows Server 2008, que puede permitir que las aplicaciones de recuperación del estado del sistema muevan, eliminen y establezcan el nombre corto de los archivos del sistema.

La herramienta Srdelayed está pensada para las aplicaciones de recuperación del estado del sistema; no reemplaza las funciones de administración de archivos. Esta herramienta solo se debe usar cuando la aplicación no puede cambiar, eliminar o establecer el nombre corto de un archivo del sistema mediante las funciones [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa), [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)y [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) . Durante el reinicio y la restauración del estado del sistema, la restauración del sistema utiliza Srdelayed.exe y la herramienta de línea de comandos wbadmin.exe para moverse, eliminar y establecer el nombre corto en ciertos archivos del sistema. Por tanto, Srdelayed puede ser útil para los desarrolladores que requieren la capacidad de restaurar estos archivos del sistema en sus propias aplicaciones de recuperación de estado del sistema.

Srdelayed puede realizar las siguientes operaciones:

-   Una operación de movimiento de archivo similar a la función [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con el retraso de MOVEFILE hasta la marca de **\_ \_ \_ reinicio**
-   Operación de eliminación de archivo similar a la función [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Una operación set de nombre corto similar a la función [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Para usar Srdelayed, la aplicación requiere la ruta de acceso completa a la ubicación del archivo de Srdelayed.exe y la ruta de acceso completa a un archivo de texto Unicode que ha creado para que contenga la información que necesita la herramienta para realizar todas las operaciones de administración de archivos que se solicitan. La aplicación es responsable de garantizar que este archivo de texto no contiene solicitudes redundantes para una operación y que controla cualquier ordenación necesaria de las operaciones de administración de archivos. Por ejemplo, como una carpeta debe estar vacía para eliminarse, la aplicación debe asegurarse de que el archivo de texto especifica la eliminación de todos los archivos dentro de la carpeta antes de solicitar que se elimine la carpeta.

Si la entrada **SetupExecute** aún no existe en el registro, la aplicación debe crear una entrada de tipo **reg \_ multi \_ SZ** denominada **SetupExecute** en la siguiente clave del registro: **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **Session Manager**.

La aplicación debe usar el siguiente formato para establecer el valor de **SetupExecute** en la ruta de acceso completa a la ubicación del archivo de Srdelayed.exe y la ruta de acceso completa a la ubicación del archivo de texto. Anteponga el prefijo " \\ \\ ?? \\ " a la ruta de acceso del archivo de texto, como se indica a continuación:

*Ruta de acceso completa a Srdelayed.exe* \\ \\ ? \\ *Ruta de acceso completa al archivo de texto*  


Por ejemplo, el siguiente valor de **SetupExecute** indica que el Srdelayed.exe se encuentra en la carpeta system32 y el archivo de texto se denomina DelayedOperations:

C: \\ Windows \\ system32 \\srdelayed.exe \\ \\ ?? \\ C: \\ temp \\ DelayedOperations  


Los espacios en la ruta de acceso y el nombre deben estar codificados en hexadecimal. Por ejemplo, para *los archivos de programa*, codifique la ruta de acceso como " \\ \\ ?? \\ \\a.dll C:Program%20Files ".

Cuando se está restaurando el registro o el sistema tras el reinicio, la aplicación debe asegurarse de que **SetupExecute** se escribe en el subárbol del registro correcto. La recuperación del registro se realiza antes de que se ejecute Srdelayed.exe. La aplicación debe escribir **SetupExecute** en la versión recuperada del registro, ya que se trata de la versión que se lee.

## <a name="format-for-the-srdelayed-input-file"></a>Formato del archivo de entrada Srdelayed

Toda la información que Srdelayed necesita para realizar operaciones de administración de archivos se especifica como una cadena de caracteres Unicode en un archivo de texto Unicode. La cadena de caracteres Unicode se divide en registros en los que cada uno de ellos se divide en cuatro campos. Cada registro especifica un único archivo de movimiento, eliminación de archivo o establecimiento de nombre corto. Los cuatro campos de cada registro contienen los parámetros de la operación. Srdelayed.exe realiza cada operación en el orden en que se producen los registros en la cadena. La aplicación debe comprobar si hay registros duplicados en este archivo y quitar los duplicados.

La cadena siguiente muestra el formato de un archivo que solicita dos operaciones y que consta de dos registros. Cada campo de parámetro termina con un solo carácter L ' \\ 0 '. Un registro se compone de cuatro campos consecutivos. \\Se anexa un carácter L ' 0 ' adicional al final de todos los registros.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


El significado de los campos de parámetros primero, segundo, tercero y cuarto depende de si el registro describe una operación de desplazamiento, eliminación o establecimiento de nombre corto.

## <a name="format-for-a-move-file-record"></a>Formato de un registro de movimiento de archivo

El campo 1 lo identifica como una solicitud para trasladar un archivo. El valor de este campo siempre es L "MoveFile" y distingue mayúsculas de minúsculas.

El campo 2 especifica la ubicación de origen del archivo. La operación Srdelayed Move File no permite mover una carpeta. Se debe especificar un archivo en este campo. El valor de este campo es la ruta de acceso completa del archivo que se anexa a " \\ \\ ?? \\ " a menos que la ruta de acceso incluya un identificador único global (GUID), que usa " \\ \\ ? \\ " como prefijo. Quite " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

El campo 3 especifica el destino del archivo. La operación de movimiento de archivo solo funciona dentro de un volumen. El origen y el destino deben estar en el mismo volumen. El valor de este campo es la ruta de acceso completa del archivo que se anexa a " \\ \\ ?? \\ " a menos que la ruta de acceso incluya un identificador único global (GUID), que usa " \\ \\ ? \\ " como prefijo. Quite " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

El campo 4 recibe información de estado de Srdelayed. El valor de este campo debe establecerse en L "NotExecuted" para un nuevo registro.

En el ejemplo siguiente se hace referencia al archivo por la ruta de acceso de la unidad. Si la ruta de acceso y el nombre del origen es C: \\ Stage \\a.dll, este registro solicita que Srdelayed lo mueva a c: \\ temp \\a.dll.

MoveFile \\ \\ ?? \\ C: \\ fase \\a.dll \\ \\ ?? \\ C: \\ temp \\a.dll NotExecuted  


En el ejemplo siguiente se hace referencia al archivo por la ruta de acceso del GUID del volumen. Si la ruta de acceso y el nombre del origen es \\ \\ ? \\ \\a.dll de la fase de volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ , este registro solicita que Srdelayed lo mueva a \\ \\ ? \\ Volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll

 MoveFile \\ \\ ?? \\a.dll de la fase de Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ \\ \\ \\ ? \\ Volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Formato de un registro de eliminación de archivo

El campo 1 lo identifica como una solicitud para eliminar un archivo. El valor de este campo siempre es L "DeleteFile" y distingue mayúsculas de minúsculas.

El campo 2 no se usa. El valor de este campo debe establecerse en L "sin usar".

El campo 3 especifica el archivo que se va a quitar. Una carpeta debe estar vacía para quitarse. Use las operaciones de eliminación de archivos para quitar todos los archivos de la carpeta antes de quitar la carpeta. El valor de este campo es la ruta de acceso completa del archivo que se anexa a " \\ \\ ?? \\ " a menos que la ruta de acceso incluya un identificador único global (GUID), que usa " \\ \\ ? \\ " como prefijo. Quite " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

El campo 4 recibe información de estado de Srdelayed. El valor de este campo debe establecerse en L "NotExecuted" para un nuevo registro.

En el ejemplo siguiente se hace referencia al archivo por la ruta de acceso de la unidad. Si la ruta de acceso y el nombre son C: \\ temp \\b.dll, este registro solicita que Srdelayed elimine el archivo.

¿No se usa DeleteFile \\ \\ ? \\ C: \\ temp \\b.dll NotExecuted  


En el ejemplo siguiente se hace referencia al archivo por GUID de volumen. Si la ruta de acceso y el nombre es \\ \\ ? \\ Volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll, este registro solicita que Srdelayed Quite el archivo.

¿No se usa DeleteFile \\ \\ ? \\ Volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Formato para Set Short-Name registro

El campo 1 lo identifica como una solicitud para establecer el nombre corto de un archivo. El valor de este campo siempre es L "SetFileShortName" y distingue mayúsculas de minúsculas.

El campo 2 especifica el nombre corto.

Campo de campo 3 especifica la ruta de acceso y el nombre largo para recibir el nombre corto. El valor de este campo es la ruta de acceso y el nombre largo del archivo que se anexa a " \\ \\ ?? \\ " a menos que la ruta de acceso incluya un identificador único global (GUID), que usa " \\ \\ ? \\ " como prefijo. Quite " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

El campo 4 recibe información de estado de Srdelayed. El valor de este campo debe establecerse en L "NotExecuted" para un nuevo registro.

En el ejemplo siguiente se hace referencia al archivo por la ruta de acceso de la unidad. Si la ruta de acceso y el nombre del archivo es C: \\ temp \\ShortFileName.dll, este registro solicita que el archivo reciba un nombre corto, shortn ~1.dll.

SetFileShortName Shortn ~1.dll \\ \\ ?? \\ C: \\ temp \\ShortFileName.dll NotExecuted  


En el ejemplo siguiente se hace referencia al archivo por GUID de volumen. Si la ruta de acceso y el nombre del archivo son \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ , este registro solicita que el archivo reciba un nombre corto, shortn ~1.dll.

SetFileShortName Shortn ~1.dll \\ \\ ?? \\ Volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Estado de las operaciones de Srdelayed

Srdelayed escribe la cadena L "SC =*xxxxxxx*" en el cuarto campo de cada registro del archivo de texto, donde *xxxxxxx* es un valor hexadecimal que indica el estado de la operación solicitada. Un valor de cero indica que la operación se realizó correctamente.

Srdelayed crea una clave del registro denominada **SystemRestore** en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** para registrar el resultado de toda la operación de restauración. Si Srdelayed realiza todas las operaciones solicitadas con éxito, el nombre RestoreStatusResult se escribe bajo esta clave con un valor cero. Si Srdelayed no puede realizar ninguna de las operaciones solicitadas, los nombres RestoreStatusResult y RestoreStatusDetails se escriben en esta clave con valores distintos de cero. El nombre RestoreStatusDetails se escribe bajo esta clave solo si Srdelayed no puede realizar ninguna operación solicitada. Si una operación para establecer el nombre corto de un archivo no se realiza correctamente, Srdelayed continúa con la siguiente operación. Srdelayed considera que las operaciones de archivo y eliminación de archivos son críticas y no continúan si una operación de movimiento o eliminación no se realiza correctamente.

 

 