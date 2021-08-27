---
description: Este material está destinado a desarrolladores que escriben sus propios programas de instalación y desarrolladores que desean obtener más información sobre las tablas de base de datos del instalador. Para obtener información general sobre el instalador, vea Acerca de Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Funciones de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6214dadc413a2c4e2d5f257c396438c850446fb9106fb70970bdb971f4653d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086215"
---
# <a name="database-functions"></a>Funciones de base de datos

Este material está destinado a desarrolladores que escriben sus propios programas de instalación y desarrolladores que desean obtener más información sobre las tablas de base de datos del instalador. Para obtener información general sobre el instalador, vea [Acerca de Windows Installer](about-windows-installer.md).

Puede usar las funciones de acceso del instalador para acceder a la base de datos y al proceso de instalación. Estas funciones solo las deben usar las acciones de instalación personalizadas y las herramientas de creación. Algunas de las funciones de acceso del instalador requieren SQL cadenas de consulta para consultar la base de datos. Las consultas deben cumplir el instalador para [SQL sintaxis](sql-syntax.md).

En este tema se enumeran las funciones de acceso a la base de datos del instalador por categoría.

## <a name="general-database-access-functions"></a>Funciones generales de acceso a bases de datos



| Función                                                             | Descripción                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Confirma los cambios en una base de datos.                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Devuelve los nombres de todas las columnas de clave principal.                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Devuelve una enumeración que describe el estado de una tabla.                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Prepara una consulta de base de datos y crea un objeto de vista.                                    |
| [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Devuelve la base de datos activa para la instalación.                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Devuelve definiciones o nombres de columna.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Abre un archivo de base de datos para el acceso a datos.                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Libera el conjunto de resultados de una vista ejecutada.                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Ejecuta la consulta de vista y proporciona los parámetros necesarios.                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Captura el siguiente registro secuencial de la vista.                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Devuelve el error que se produjo en [**la función MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Actualiza un registro obtenido.                                                               |



 

## <a name="database-management-functions"></a>Funciones de administración de bases de datos



| Función                                                               | Descripción                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Crea información de resumen para una transformación existente.           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Aplica una transformación a una base de datos.                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Exporta una tabla de una base de datos abierta a un archivo de archivo de texto.    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Genera un archivo de transformación de diferencias entre dos bases de datos. |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importa una tabla de archivo de texto del instalador en una base de datos abierta.   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Combina dos bases de datos.                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Devuelve el estado de la base de datos.                               |



 

## <a name="record-processing-functions"></a>Funciones de procesamiento de registros



| Función                                                 | Descripción                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Crea un nuevo objeto de registro con el número especificado de campos.      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Da formato a los datos y propiedades de los campos de registro mediante una cadena de formato. |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Establece todos los campos de un registro en NULL.                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Devuelve la longitud de un campo de registro.                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Devuelve el número de campos de un registro.                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Devuelve el valor entero de un campo de registro.                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Devuelve el valor de cadena de un campo de registro.                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Informa de si un campo de registro es NULL.                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Lee bytes de un campo de secuencia de registros en un búfer.           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Establece un campo de registro en un campo entero.                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Establece un campo de flujo de registros de un archivo.                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Copia una cadena en el campo designado.                      |



 

## <a name="summary-information-property-functions"></a>Funciones de propiedades de información de resumen



| Función                                                                 | Descripción                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Obtiene el identificador para el flujo de información de resumen de la base de datos del instalador.    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Obtiene una sola propiedad de la información de resumen.                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Devuelve el número de propiedades del flujo de información de resumen.        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Escribe la información de resumen modificada en el flujo de información de resumen. |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Establece una única propiedad de información de resumen.                            |



 

## <a name="installer-state-access-functions"></a>Funciones de acceso de estado del instalador



| Función                                               | Descripción                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Devuelve el idioma numérico de la instalación actual.   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Devuelve el registro de error devuelto por última vez para el proceso de llamada. |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Devuelve uno de los estados de instalación interna booleanos.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Obtiene el valor de una propiedad del instalador.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Establece el valor de una propiedad de instalación.                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Establece un estado booleano del motor interno.                      |



 

## <a name="installer-action-functions"></a>Funciones de acción del instalador



| Función                                             | Descripción                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Ejecuta una acción integrada, una acción personalizada o una acción del asistente de interfaz de usuario. |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Evalúa una expresión condicional que contiene valores y nombres de propiedad.  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Envía un registro de error al instalador para su procesamiento.                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Ejecuta una secuencia de acciones.                                              |



 

## <a name="installer-location-functions"></a>Funciones de ubicación del instalador



| Función                                     | Descripción                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Devuelve la ruta de acceso de origen completa de una carpeta de la tabla Directory. |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Devuelve la ruta de acceso de destino completa de una carpeta de la tabla Directory. |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Establece la ruta de acceso de destino completa de una carpeta de la tabla Directory.    |



 

## <a name="installer-selection-functions"></a>Funciones de selección del instalador



| Función                                                     | Descripción                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Enumera el espacio en disco por unidad necesario para instalar un componente. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Obtiene el estado de un componente.                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Devuelve el espacio en disco requerido por una característica.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Obtiene el estado de una característica.                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Devuelve un estado de instalación válido.                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Establece un componente en el estado especificado.                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Modifica los atributos predeterminados de una característica en tiempo de ejecución.            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Establece una característica en un estado especificado.                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Establece el nivel de instalación de una instalación completa del producto.          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Comprueba si hay suficiente espacio en disco.                                    |



 

## <a name="user-interface-functions"></a>Interfaz de usuario functions



| Función                                           | Descripción                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Habilita el modo de vista previa de la interfaz de usuario.                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Muestra un cuadro de diálogo con el control host en el cuadro de diálogo mostrado. |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Muestra un cuadro de diálogo como modelador e inactivo.                         |



 

Todas las funciones admiten llamadas ANSI y Unicode. Para usar estas funciones, incluya MsiQuery.h y vincule con Msi.lib.

## <a name="installation-functions"></a>Funciones de instalación

Además de las funciones de acceso a la base de datos enumeradas anteriormente, puede crear un paquete de instalación para una aplicación mediante las funciones del instalador enumeradas en la sección Referencia de función [del](installer-function-reference.md) instalador.

 

 



