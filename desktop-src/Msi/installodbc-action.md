---
description: La acción InstallODBC instala los controladores, los traductores y los orígenes de datos en la tabla ODBCDriver, la tabla ODBCTranslator y la tabla ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Acción InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688448"
---
# <a name="installodbc-action"></a>Acción InstallODBC

La acción InstallODBC instala los controladores, los traductores y los orígenes de datos en la tabla [ODBCDriver](odbcdriver-table.md), la tabla [ODBCTranslator](odbctranslator-table.md)y la tabla [ODBCDataSource](odbcdatasource-table.md). Si ya existe un controlador o un traductor, la acción InstallODBC realiza las llamadas a SQL necesarias para la instalación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallODBC no copia ni quita archivos, y debe ser después de acciones que copian o quitan archivos.

## <a name="actiondata-messages"></a>Mensajes ActionData

En la tabla siguiente se identifican los mensajes de ActionData para cada controlador instalado.



| Campo       | Descripción                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descripción del controlador. La clave del controlador ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Carpeta.                                                                  |
| \[4, 5,...\] | Pares de atributo y valor de [ODBCAttribute](odbcattribute-table.md). |



 

En la tabla siguiente se identifican los mensajes de ActionData para cada traductor instalado.



| Campo       | Descripción                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descripción del controlador. La clave del controlador ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Carpeta.                                                                  |
| \[4, 5,...\] | Pares de atributo y valor de [ODBCAttribute](odbcattribute-table.md). |



 

En la tabla siguiente se identifican los mensajes ActionData de cada origen de datos instalado.



| Campo       | Descripción                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descripción del controlador. La clave del controlador ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Registro: ODBC \_ Add \_ DSN u ODBC \_ Add \_ Sys \_ DSN.                     |
| \[4, 5,...\] | Pares de atributo y valor de [ODBCAttribute](odbcattribute-table.md). |



 

## <a name="remarks"></a>Observaciones

El administrador de controladores ODBC debe estar creado en el paquete de Microsoft Installer y debe incluirse un componente denominado ODBCDriverManager. Si es necesario, el administrador se instala.

Para cambiar el nombre del componente, establezca una propiedad denominada ODBCDriverManager en el nuevo nombre del componente. Si se va a instalar el administrador de controladores ODBC de 64 bits, el componente que lo lleva debe denominarse ODBCDriverManager64.

-   La acción InstallODBC consulta la [tabla ODBCDataSource](odbcdatasource-table.md) y la [tabla ODBCSourceAttribute](odbcsourceattribute-table.md) de cada origen de datos que se va a instalar, así como los atributos del origen de datos.
-   La acción InstallODBC consulta la [tabla ODBCDriver](odbcdriver-table.md) y la [tabla ODBCTranslator](odbctranslator-table.md) para cada controlador y traductor que se selecciona para su instalación.
-   La acción InstallODBC consulta en la [tabla ODBCAttribute](odbcattribute-table.md) los atributos de los controladores y traductores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Windows Installer](windows-installer-examples.md)
</dt> </dl>

 

 



