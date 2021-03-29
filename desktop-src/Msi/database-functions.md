---
description: Este material está dirigido a desarrolladores que escriben sus propios programas de configuración y desarrolladores que desean obtener más información acerca de las tablas de base de datos del instalador. Para obtener información general sobre el instalador, vea acerca de Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Funciones de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810748"
---
# <a name="database-functions"></a>Funciones de base de datos

Este material está dirigido a desarrolladores que escriben sus propios programas de configuración y desarrolladores que desean obtener más información acerca de las tablas de base de datos del instalador. Para obtener información general sobre el instalador, vea [acerca de Windows Installer](about-windows-installer.md).

Puede usar las funciones de acceso del instalador para tener acceso a la base de datos y al proceso de instalación. Estas funciones solo deben usarse con acciones de instalación personalizadas y herramientas de creación. Algunas de las funciones de acceso del instalador requieren cadenas de consulta SQL para consultar la base de datos. Las consultas deben adherirse a la [Sintaxis de SQL](sql-syntax.md)del instalador.

En este tema se enumeran las funciones de acceso a bases de datos de instalador por categoría.

## <a name="general-database-access-functions"></a>Funciones generales de acceso a bases de datos



| Función                                                             | Descripción                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Confirma los cambios en una base de datos.                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Devuelve los nombres de todas las columnas de clave principal.                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Devuelve una enumeración que describe el estado de una tabla.                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Prepara una consulta de base de datos y crea un objeto de vista.                                    |
| [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Devuelve la base de datos activa para la instalación.                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Devuelve nombres o definiciones de columna.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Abre un archivo de base de datos para el acceso a datos.                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Libera el conjunto de resultados para una vista ejecutada.                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Ejecuta la consulta de vista y proporciona los parámetros necesarios.                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Captura el siguiente registro secuencial de la vista.                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Devuelve el error que se produjo en la función [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) . |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Actualiza un registro capturado.                                                               |



 

## <a name="database-management-functions"></a>Funciones de administración de bases de datos



| Función                                                               | Descripción                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Crea información de resumen para una transformación existente.           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Aplica una transformación a una base de datos.                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Exporta una tabla de una base de datos abierta a un archivo de almacenamiento de texto.    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Genera un archivo de transformación de diferencias entre dos bases de datos. |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importa una tabla de archivo de texto del instalador en una base de datos abierta.   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Combina dos bases de datos juntas.                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Devuelve el estado de la base de datos.                               |



 

## <a name="record-processing-functions"></a>Funciones de procesamiento de registros



| Función                                                 | Descripción                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Crea un nuevo objeto record con el número de campos especificado.      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Da formato a las propiedades y los datos de los campos de registro mediante una cadena de formato. |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Establece todos los campos de un registro en NULL.                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Devuelve la longitud de un campo de registro.                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Devuelve el número de campos de un registro.                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Devuelve el valor entero de un campo de registro.                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Devuelve el valor de cadena de un campo de registro.                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Indica si un campo de registro es NULL.                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Lee los bytes de un campo de flujo de registro en un búfer.           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Establece un campo de registro en un campo de tipo entero.                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Establece un campo de flujo de registro de un archivo.                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Copia una cadena en el campo designado.                      |



 

## <a name="summary-information-property-functions"></a>Funciones de propiedad de información de Resumen



| Función                                                                 | Descripción                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Obtiene el identificador del flujo de información de Resumen de la base de datos del instalador.    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Obtiene una única propiedad de la información de resumen.                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Devuelve el número de propiedades de la secuencia de información de resumen.        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Vuelve a escribir la información de Resumen modificada en el flujo de información de resumen. |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Establece una propiedad de información de Resumen única.                            |



 

## <a name="installer-state-access-functions"></a>Funciones de acceso de estado del instalador



| Función                                               | Descripción                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Devuelve el idioma numérico de la instalación actual.   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Devuelve el registro de errores devuelto por última vez para el proceso de llamada. |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Devuelve uno de los Estados de instalación interna booleano.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Obtiene el valor de una propiedad del instalador.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Establece el valor de una propiedad de instalación.                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Establece un estado booleano del motor interno.                      |



 

## <a name="installer-action-functions"></a>Funciones de acción del instalador



| Función                                             | Descripción                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Ejecuta una acción integrada, una acción personalizada o una acción del Asistente para la interfaz de usuario. |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Evalúa una expresión condicional que contiene nombres y valores de propiedad.  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Envía un registro de error al instalador para su procesamiento.                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Ejecuta una secuencia de acción.                                              |



 

## <a name="installer-location-functions"></a>Funciones de ubicación del instalador



| Función                                     | Descripción                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Devuelve la ruta de acceso de origen completa de una carpeta de la tabla de directorio. |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Devuelve la ruta de acceso de destino completa de una carpeta de la tabla de directorio. |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Establece la ruta de acceso de destino completa para una carpeta en la tabla de directorio.    |



 

## <a name="installer-selection-functions"></a>Funciones de selección del instalador



| Función                                                     | Descripción                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Enumera el espacio en disco por unidad necesaria para instalar un componente. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Obtiene el estado de un componente.                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Devuelve el espacio en disco requerido por una característica.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Obtiene el estado de una característica.                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Devuelve un estado de instalación válido.                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Establece un componente en el estado especificado.                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Modifica los atributos predeterminados de una característica en tiempo de ejecución.            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Establece una característica en un estado especificado.                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Establece el nivel de instalación de una instalación completa del producto.          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Comprueba si hay suficiente espacio en disco.                                    |



 

## <a name="user-interface-functions"></a>Funciones de la interfaz de usuario



| Función                                           | Descripción                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Habilita el modo de vista previa de la interfaz de usuario.                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Muestra una cartelera con el control host en el cuadro de diálogo que se muestra. |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Muestra un cuadro de diálogo como no modal e inactivo.                         |



 

Todas las funciones admiten llamadas ANSI y Unicode. Para usar estas funciones, incluya MsiQuery. h y vincule con MSI. lib.

## <a name="installation-functions"></a>Funciones de instalación

Además de las funciones de acceso a bases de datos mencionadas anteriormente, se crea un paquete de instalación para una aplicación mediante las funciones del instalador enumeradas en la sección referencia de la [función del instalador](installer-function-reference.md) .

 

 



