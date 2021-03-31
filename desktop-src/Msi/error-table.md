---
description: La tabla de errores se usa para buscar plantillas de formato de mensajes de error al procesar errores con un conjunto de códigos de error, pero sin un conjunto de plantillas de formato (esta es la situación normal).
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: Tabla de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277176"
---
# <a name="error-table"></a>Tabla de errores

La tabla de errores se usa para buscar plantillas de formato de mensajes de error al procesar errores con un conjunto de códigos de error, pero sin un conjunto de plantillas de formato (esta es la situación normal).

La tabla de errores tiene las columnas siguientes.



| Columna  | Tipo                     | Clave | Nullable |
|---------|--------------------------|-----|----------|
| Error   | [Entero](integer.md)   | Y   | N        |
| Message | [Plantilla](template.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error
</dt> <dd>

Consulte [Windows Installer mensajes de error](windows-installer-error-messages.md) para obtener una lista de los números de error y mensajes.

El número de error debe ser un entero no negativo.

El intervalo de 25000 a 30000 se reserva para los errores de acciones personalizadas. Los autores de acciones personalizadas pueden utilizar este intervalo para sus acciones personalizadas.

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>Mensaje
</dt> <dd>

Esta columna contiene la plantilla de formato de error traducible. El proceso de compilación inicial genera la tabla de errores que contiene las plantillas de formato de depuración.

En la tabla siguiente se enumeran los mensajes reservados. Para obtener una lista de los códigos de error internos, consulte [Windows Installer mensajes de error](windows-installer-error-messages.md).



| Error | Message                                                    | Observaciones                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{Error irrecuperable:}}                                          | Prefijo de encabezado para errores irrecuperables (INSTALLMESSAGE \_ FATALEXIT). El texto incluido entre llaves dobles {{Text}} solo está visible en el archivo de registro. El texto no se muestra al usuario en la interfaz de usuario.                  |
| 1     | Error \[ 1 \] .                                               | Prefijo de encabezado para errores (error de INSTALLMESSAGE \_ )                                                                                                                                                             |
| 2     | ADVERTENCIA \[ 1 \] .                                             | Prefijo de encabezado para advertencias (ADVERTENCIA de INSTALLMESSAGE \_ )                                                                                                                                                         |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | Información \[ 1 \] .                                                | Prefijo de encabezado para mensajes informativos (información de INSTALLMESSAGE \_ )                                                                                                                                              |
| 5     | Error interno \[ 1 \] . \[2 \] {, \[ 3 \] } {, \[ 4 \] }              | Prefijo de encabezado para errores internos                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{Disk Full:}}                                            | Prefijo de encabezado para errores de espacio insuficiente en disco (INSTALLMESSAGE \_ OUTOFDISKSPACE). El texto incluido entre llaves dobles {{Text}} solo está visible en el archivo de registro. El texto no se muestra al usuario en la interfaz de usuario. |
| 8     | Tiempo de acción \[ \] : \[ 1 \] . \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] } { \[ ,3 \] } {, \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | Tipo de mensaje: \[ 1 \] , argumento: \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | = = = Registro iniciado: \[ fecha y \] \[ hora\] ===                 |                                                                                                                                                                                                              |
| 13    | = = = Registro detenido: \[ fecha y \] \[ hora\] ===                 |                                                                                                                                                                                                              |
| 14    | Hora de inicio de la acción \[ \] : \[ 1\]                               |                                                                                                                                                                                                              |
| 15    | Hora de finalización de la acción \[ \] : \[ 1 \] . Valor devuelto \[ 2\]           |                                                                                                                                                                                                              |
| 16    | Tiempo restante: { \[ 1 \] min} { \[ 2 \] s}                    |                                                                                                                                                                                                              |
| 17    | Memoria insuficiente Cerrar otras aplicaciones antes de volver a intentarlo |                                                                                                                                                                                                              |
| 18    | El instalador ya no responde                          |                                                                                                                                                                                                              |
| 19    | El instalador terminó prematuramente                           |                                                                                                                                                                                                              |
| 20    | Espere mientras Windows configura \[ ProductName \] ...    |                                                                                                                                                                                                              |
| 21    | Recopilando información necesaria...                          |                                                                                                                                                                                                              |
| 22    | Quitando versiones anteriores de esta aplicación...             |                                                                                                                                                                                                              |
| 23    | Preparando la eliminación de las versiones anteriores de esta aplicación...  |                                                                                                                                                                                                              |
| 32    | La \[ instalación de {ProductName \] } se completó correctamente.            |                                                                                                                                                                                                              |
| 33    | Error en el programa de instalación de { \[ ProductName \] }.                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La plantilla no incluye el formato del número de error en el campo 1. Al procesar el error, el instalador adjunta un prefijo de encabezado a la plantilla en función del tipo de mensaje. Estos encabezados también se almacenan en la tabla de errores.

El texto incluido entre llaves dobles {{Text}} solo está visible en el archivo de registro. El texto no se muestra al usuario en la interfaz de usuario.

Puede importar una tabla de errores localizada en la base de datos mediante Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). El SDK incluye una tabla de errores localizada para cada uno de los idiomas que aparecen en la sección [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) . Si no se rellena la tabla de errores, el instalador carga las cadenas localizadas para el idioma especificado por la propiedad [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



