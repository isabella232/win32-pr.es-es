---
title: Srdelayed.exe
description: Es posible que las aplicaciones que realizan operaciones de restauración del estado del sistema al principio del inicio del sistema operativo no puedan usar las funciones de administración de archivos para mover, eliminar o establecer el nombre corto de determinados archivos del sistema.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe Backup
- copia de seguridad de recuperación de estado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdf95ff77fd17a578b85e6037c71146666eae9522d066bc1c4629fb9a2c24e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835543"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Es posible que las aplicaciones que realizan operaciones de restauración del estado del sistema al principio del inicio del sistema operativo no puedan usar las funciones de administración de archivos para mover, eliminar o establecer el nombre corto de determinados archivos del sistema. Srdelayed.exe es un archivo ejecutable, proporcionado con la característica copia de seguridad de Windows Server (WSB) en Windows Server 2008, que puede permitir que las aplicaciones de recuperación de estado del sistema muevan, eliminen y establezcan el nombre corto de los archivos del sistema.

La herramienta Srdelayed está pensada para aplicaciones de recuperación de estado del sistema; no reemplaza las funciones de administración de archivos. Esta herramienta solo se debe usar cuando la aplicación no puede mover, eliminar o establecer el nombre corto de un archivo del sistema mediante las funciones [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa), [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)y [**SetFileShortName.**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) Durante una restauración y reinicio del estado del sistema, Restaurar sistema y la herramienta de línea de comandos wbadmin.exe usan Srdelayed.exe para mover, eliminar y establecer el nombre corto en determinados archivos del sistema. Por lo tanto, Srplayed puede ser útil para los desarrolladores que requieren la capacidad de restaurar estos archivos del sistema en sus propias aplicaciones de recuperación de estado del sistema.

Srdelayed puede realizar las siguientes operaciones:

-   Una operación de mover archivo similar a la [**función MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con la **marca MOVEFILE DELAY UNTIL \_ \_ \_ REBOOT**
-   Una operación de eliminación de archivos similar a [**la función DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Una operación de nombre corto de conjunto similar a la [**función SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Para usar Srdelayed, la aplicación requiere la ruta de acceso completa a la ubicación del archivo Srdelayed.exe y la ruta de acceso completa a un archivo de texto Unicode que haya escrito para contener la información que la herramienta necesita para realizar todas las operaciones de administración de archivos que se solicitan. La aplicación es responsable de garantizar que este archivo de texto no contiene solicitudes redundantes para una operación y que controla cualquier ordenación necesaria de las operaciones de administración de archivos. Por ejemplo, dado que una carpeta debe estar vacía para eliminarse, la aplicación debe asegurarse de que el archivo de texto especifica la eliminación de todos los archivos dentro de la carpeta antes de solicitar la eliminación de la carpeta.

Si la **entrada SetupExecute** aún no existe en el Registro, la aplicación debe crear una entrada de tipo **REG MULTI \_ \_ SZ** denominada **SetupExecute** bajo la siguiente clave del Registro: **HKEY LOCAL \_ \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

La aplicación debe usar el formato siguiente para establecer el valor de **SetupExecute** en la ruta de acceso completa a la ubicación del archivo Srdelayed.exe y la ruta de acceso completa a la ubicación del archivo de texto. Prefijo \\ \\ "?? \\ " en la ruta de acceso del archivo de texto, como se muestra a continuación:

*Ruta de acceso completa Srdelayed.exe* \\ \\ ?? \\ *Ruta de acceso completa al archivo de texto*  


Por ejemplo, el siguiente valor de **SetupExecute** indica que el Srdelayed.exe se encuentra en la carpeta System32 y el archivo de texto se denomina DelayedOperations:

C: \\ Windows \\ System32 \\srdelayed.exe \\ \\ ?? \\ C: \\ temp \\ DelayedOperations  


Los espacios de la ruta de acceso y el nombre deben estar codificados hexadecimalmente. Por ejemplo, para *Archivos de programa*, codifica la ruta de acceso como \\ \\ "?? \\ C:Program%20Files \\a.dll".

Cuando el registro o el sistema se restauran al reiniciarse, la aplicación debe asegurarse de que **SetupExecute** se escribe en el subárbol del Registro correcto. La recuperación del registro se realiza antes Srdelayed.exe se ejecuta. La aplicación debe escribir **SetupExecute en** la versión recuperada del Registro porque es la versión que se lee.

## <a name="format-for-the-srdelayed-input-file"></a>Formato del archivo de entrada retrasada

Toda la información que Srdelayed necesita para realizar operaciones de administración de archivos se especifica como una cadena de caracteres Unicode en un archivo de texto Unicode. La cadena de caracteres Unicode se divide en registros que se particionan en cuatro campos. Cada registro especifica un único archivo de movimiento, eliminación o operación de nombre corto. Los cuatro campos de cada registro contienen los parámetros de la operación. Srdelayed.exe realiza cada operación en el orden en que sus registros se producen en la cadena. La aplicación debe comprobar si hay registros duplicados en este archivo y quitar los duplicados.

La cadena siguiente muestra el formato de un archivo que solicita dos operaciones y consta de dos registros. Cada campo de parámetro termina con un solo carácter L' \\ 0'. Un registro se compone de cuatro campos consecutivos. Se anexa un carácter L' 0' adicional al \\ final de todos los registros.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


El significado de los campos de primer, segundo, tercero y cuarto parámetro depende de si el registro describe una operación de mover, eliminar o establecer un nombre corto.

## <a name="format-for-a-move-file-record"></a>Formato de un registro de mover archivo

El campo 1 lo identifica como una solicitud para mover un archivo. El valor de este campo siempre es L"MoveFile" y distingue mayúsculas de minúsculas.

El campo 2 especifica la ubicación de origen del archivo. La operación de archivo de movimiento retrasado no admite el movimiento de una carpeta. Se debe especificar un archivo en este campo. El valor de este campo es la ruta de acceso completa del archivo anexado a " ?? " a menos que la ruta de acceso incluya un identificador único \\ \\ \\ global (GUID), que usa " \\ \\ ? " \\ como prefijo. Quite " \\ \\ ? " antes de \\ anexar a " \\ \\ ?? \\ ".

El campo 3 especifica el destino del archivo. La operación de movimiento de archivos solo funciona dentro de un volumen. El origen y el destino deben estar en el mismo volumen. El valor de este campo es la ruta de acceso completa del archivo anexado a " ?? " a menos que la ruta de acceso incluya un identificador único \\ \\ \\ global (GUID), que usa " \\ \\ ? " \\ como prefijo. Quite " \\ \\ ? " antes de \\ anexar a " \\ \\ ?? \\ ".

El campo 4 recibe información de estado de Srdelayed. El valor de este campo debe establecerse en L "NotExecuted" para un nuevo registro.

En el ejemplo siguiente se hace referencia al archivo por ruta de acceso de unidad. Si la ruta de acceso y el nombre del origen son C: Fasea.dll, este registro solicita que S pathlayed la mueva \\ \\ a C: temp \\ \\a.dll.

MoveFile \\ \\ ?? \\ C: \\ Fase \\a.dll \\ \\ ?? \\ C: \\ temp \\a.dll NotExecuted  


En el ejemplo siguiente se hace referencia al archivo por ruta de acceso GUID de volumen. Si la ruta de acceso y el nombre del origen son \\ \\ ? \\ Volumen{26a21bda-a627-11d7-9931-806e6f6e6e6963} Stagea.dll, este registro solicita que \\ \\ Srdelayed lo mueva a \\ \\ ? \\ Volumen{26a21bda-a627-11d7-9931-806e6f6e6e6963} \\ temp \\a.dll

 MoveFile \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ Stage \\a.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Formato de un registro de eliminación de archivos

El campo 1 lo identifica como una solicitud para eliminar un archivo. El valor de este campo siempre es L"DeleteFile" y distingue mayúsculas de minúsculas.

El campo 2 no se usa. El valor de este campo debe establecerse en L"Sin usar".

El campo 3 especifica el archivo que se va a quitar. Una carpeta debe estar vacía para quitarse. Use las operaciones de eliminación de archivos para quitar todos los archivos de la carpeta antes de quitar la carpeta. El valor de este campo es la ruta de acceso completa del archivo anexado a " ?? " a menos que la ruta de acceso incluya un identificador único \\ \\ \\ global (GUID), que usa " \\ \\ ? " \\ como prefijo. Quite " \\ \\ ? " antes de \\ anexar a " \\ \\ ?? \\ ".

El campo 4 recibe información de estado de Srdelayed. El valor de este campo debe establecerse en L "NotExecuted" para un nuevo registro.

En el ejemplo siguiente se hace referencia al archivo por ruta de acceso de unidad. Si la ruta de acceso y el nombre son C: tempb.dll, este registro solicita que \\ \\ S pathlayed elimine el archivo.

DeleteFile Unused \\ \\ ?? \\ C: \\ temp \\b.dll NotExecuted  


En el ejemplo siguiente se hace referencia al archivo por GUID de volumen. Si la ruta de acceso y el nombre son \\ \\ ? \\ Volumen{26a21bda-a627-11d7-9931-806e6f6e6e6963} tempb.dll, este registro solicita que \\ \\ Sevalayed quite el archivo.

DeleteFile Unused \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Formato para Establecer Short-Name registro

El campo 1 lo identifica como una solicitud para establecer el nombre corto de un archivo. El valor de este campo siempre es L"SetFileShortName" y distingue mayúsculas de minúsculas.

El campo 2 especifica el nombre corto.

El campo 3 especifica la ruta de acceso y el nombre largo para recibir el nombre corto. El valor de este campo es la ruta de acceso y el nombre largo del archivo anexado a " ?? " a menos que la ruta de acceso incluya un identificador único \\ \\ \\ global (GUID), que usa " \\ \\ ? " \\ como prefijo. Quite " \\ \\ ? " antes de \\ anexar a " \\ \\ ?? \\ ".

El campo 4 recibe información de estado de Srdelayed. El valor de este campo debe establecerse en L "NotExecuted" para un nuevo registro.

En el ejemplo siguiente se hace referencia al archivo por ruta de acceso de unidad. Si la ruta de acceso y el nombre del archivo son C: tempShortFileName.dll, este registro solicita que el archivo reciba un nombre \\ \\ corto, ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ C: \\ temp \\ShortFileName.dll NotExecuted  


En el ejemplo siguiente se hace referencia al archivo por GUID de volumen. Si la ruta de acceso y el nombre del archivo es \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} tempShortFileName.dll, este registro solicita que el archivo reciba un nombre \\ \\ \\ corto, ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ Volumen{26a21bda-a627-11d7-9931-806e6f6e6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Estado de las operaciones retrasadas

Srdelayed escribe la cadena L"SC=*xxxxxxx*" en el cuarto campo de cada registro del archivo de texto, donde *xxxxxxx* es un hexadecimal que indica el estado de la operación solicitada. Un valor de cero indica que la operación se ha correcto.

Srdelayed crea una clave del Registro denominada **SystemRestore** en **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** Windows \\ **NT** \\ **CurrentVersion** para registrar el resultado de toda la operación de restauración. Si Srdelayed realiza todas las operaciones solicitadas correctamente, el nombre RestoreStatusResult se escribe debajo de esta clave con un valor cero. Si Srdelayed no puede realizar ninguna de las operaciones solicitadas, los nombres RestoreStatusResult y RestoreStatusDetails se escriben en esta clave con valores distintos de cero. El nombre RestoreStatusDetails se escribe con esta clave solo si Srdelayed no puede realizar ninguna operación solicitada. Si una operación para establecer el nombre corto de un archivo no se realiza correctamente, Srdelayed continúa con la siguiente operación. S continuelayed considera que las operaciones de archivo de movimiento y eliminación son críticas y no continúa si una operación de movimiento o eliminación no se realiza correctamente.

 

 