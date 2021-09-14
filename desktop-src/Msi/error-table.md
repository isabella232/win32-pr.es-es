---
description: La tabla Error se usa para buscar plantillas de formato de mensajes de error al procesar errores con un código de error establecido pero sin un conjunto de plantillas de formato (esta es la situación normal).
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: Tabla de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158454"
---
# <a name="error-table"></a>Tabla de errores

La tabla Error se usa para buscar plantillas de formato de mensajes de error al procesar errores con un código de error establecido pero sin un conjunto de plantillas de formato (esta es la situación normal).

La tabla Error tiene las columnas siguientes.



| Columna  | Tipo                     | Clave | Nullable |
|---------|--------------------------|-----|----------|
| Error   | [Entero](integer.md)   | Y   | N        |
| Message | [Plantilla](template.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error
</dt> <dd>

Vea [Windows mensajes de error del instalador](windows-installer-error-messages.md) para obtener una lista de los números de error y los mensajes.

El número de error debe ser un entero no negativo.

El intervalo de 25 000 a 30 000 está reservado para los errores de las acciones personalizadas. Los autores de acciones personalizadas pueden usar este intervalo para sus acciones personalizadas.

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>Mensaje
</dt> <dd>

Esta columna contiene la plantilla de formato de error localizable. El proceso de compilación inicial genera la tabla Error para contener las plantillas de formato de depuración.

En la tabla siguiente se enumeran los mensajes reservados. Para obtener una lista de códigos de error internos y de envío, [Windows mensajes de error del instalador](windows-installer-error-messages.md).



| Error | Message                                                    | Observaciones                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{Error irreales: }}                                          | Prefijo de encabezado para errores irrecontencionables (INSTALLMESSAGE \_ FATALEXIT). El texto entre llaves dobles {{text}} solo está visible en el archivo de registro. El texto no se muestra al usuario en la interfaz de usuario.                  |
| 1     | Error \[ 1 \] .                                               | Prefijo de encabezado para errores (INSTALLMESSAGE \_ ERROR)                                                                                                                                                             |
| 2     | Advertencia \[ 1 \] .                                             | Prefijo de encabezado para advertencias (INSTALLMESSAGE \_ WARNING)                                                                                                                                                         |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | Información \[ 1 \] .                                                | Prefijo de encabezado para mensajes informativos (INSTALLMESSAGE \_ INFO)                                                                                                                                              |
| 5     | Error \[ interno 1 \] . \[2 \] {, \[ 3 \] }{, \[ 4 \] }              | Prefijo de encabezado para errores internos                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{Disco lleno: }}                                            | Prefijo de encabezado para errores de espacio fuera del disco (INSTALLMESSAGE \_ OUTOFDISKSPACE). El texto entre llaves dobles {{text}} solo está visible en el archivo de registro. El texto no se muestra al usuario en la interfaz de usuario. |
| 8     | Tiempo \[ de \] acción: \[ 1 \] . \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] }{, \[ 3 \] }{, \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | Tipo de mensaje: \[ 1 \] , Argumento: \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | === Registro iniciado: \[ fecha \] \[ y hora\] ===                 |                                                                                                                                                                                                              |
| 13    | === Registro detenido: \[ fecha \] \[ y hora\] ===                 |                                                                                                                                                                                                              |
| 14    | Hora de inicio \[ de \] la \[ acción: 1\]                               |                                                                                                                                                                                                              |
| 15    | Hora de fin \[ de \] la acción: \[ 1 \] . Valor devuelto \[ 2\]           |                                                                                                                                                                                                              |
| 16    | Tiempo restante: { \[ 1 \] min }{ \[ 2 \] s}                    |                                                                                                                                                                                                              |
| 17    | Memoria insuficiente Apagar otras aplicaciones antes de reintentar |                                                                                                                                                                                                              |
| 18    | El instalador ya no responde                          |                                                                                                                                                                                                              |
| 19    | El instalador finalizó prematuramente                           |                                                                                                                                                                                                              |
| 20    | Espere mientras Windows \[ \] productName...    |                                                                                                                                                                                                              |
| 21    | Recopilación de la información necesaria...                          |                                                                                                                                                                                                              |
| 22    | Quitar versiones anteriores de esta aplicación...             |                                                                                                                                                                                                              |
| 23    | Preparar la eliminación de versiones anteriores de esta aplicación...  |                                                                                                                                                                                                              |
| 32    | { \[ ProductName \] }El programa de instalación se completó correctamente.            |                                                                                                                                                                                                              |
| 33    | { \[ ProductName \] }Error de instalación.                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La plantilla no incluye el formato del número de error en el campo 1. Al procesar el error, el instalador asocia un prefijo de encabezado a la plantilla en función del tipo de mensaje. Estos encabezados también se almacenan en la tabla Error.

El texto entre llaves dobles {{text}} solo está visible en el archivo de registro. El texto no se muestra al usuario en la interfaz de usuario.

Puede importar una tabla error localizada en la base de datos mediante Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). El SDK incluye una tabla de errores localizada para cada uno de los idiomas enumerados en la sección Localización de las tablas [Error y ActionText.](localizing-the-error-and-actiontext-tables.md) Si no se rellena la tabla Error, el instalador carga cadenas localizadas para el idioma especificado por la [**propiedad ProductLanguage.**](productlanguage.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



