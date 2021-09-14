---
description: La acción InstallODBC instala los controladores, traductores y orígenes de datos en la tabla ODBCDriver, la tabla ODBCTranslator y la tabla ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Acción InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072036"
---
# <a name="installodbc-action"></a>Acción InstallODBC

La acción InstallODBC instala los controladores, traductores y orígenes de datos en las tablas [ODBCDriver,](odbcdriver-table.md) [ODBCTranslator y](odbctranslator-table.md) [ODBCDataSource](odbcdatasource-table.md). Si ya existe un controlador o traductor, la acción InstallODBC realiza SQL llamadas necesarias para la instalación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallODBC no copia ni quita archivos, y debe ser después de las acciones que copian o quitan archivos.

## <a name="actiondata-messages"></a>Mensajes ActionData

En la tabla siguiente se identifican los mensajes ActionData para cada controlador instalado.



| Campo       | Descripción                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descripción del controlador. Clave del controlador ODBC.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Carpeta.                                                                  |
| \[4, 5, ...\] | Pares de atributo y valor [de ODBCAttribute.](odbcattribute-table.md) |



 

En la tabla siguiente se identifican los mensajes ActionData para cada traductor instalado.



| Campo       | Descripción                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descripción del controlador. Clave del controlador ODBC.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Carpeta.                                                                  |
| \[4, 5, ...\] | Pares de atributo y valor [de ODBCAttribute.](odbcattribute-table.md) |



 

En la tabla siguiente se identifican los mensajes ActionData para cada origen de datos instalado.



| Campo       | Descripción                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descripción del controlador. Clave del controlador ODBC.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Registro: ODBC \_ ADD \_ DSN u ODBC \_ ADD SYS \_ \_ DSN.                     |
| \[4, 5, ...\] | Pares de atributo y valor [de ODBCAttribute.](odbcattribute-table.md) |



 

## <a name="remarks"></a>Observaciones

El Administrador de controladores ODBC debe crearse en el paquete de Microsoft Installer y se debe incluir un componente denominado ODBCDriverManager. El administrador se instala si es necesario.

Para cambiar el nombre del componente, establezca una propiedad denominada ODBCDriverManager en el nuevo nombre del componente. Si se va a instalar un Administrador de controladores ODBC de 64 bits, el componente que lo incluye debe denominarse ODBCDriverManager64.

-   La acción InstallODBC consulta la tabla [ODBCDataSource](odbcdatasource-table.md) y la tabla [ODBCSourceAttribute](odbcsourceattribute-table.md) para cada origen de datos que se va a instalar y los atributos del origen de datos.
-   La acción InstallODBC consulta la tabla [ODBCDriver](odbcdriver-table.md) y la tabla [ODBCTranslator](odbctranslator-table.md) para cada controlador y traductor seleccionados para la instalación.
-   La acción InstallODBC consulta la tabla [ODBCAttribute para](odbcattribute-table.md) los atributos de los controladores y traductores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Ejemplos del instalador](windows-installer-examples.md)
</dt> </dl>

 

 



