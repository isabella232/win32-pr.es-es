---
description: Modifique cualquiera de las demás columnas localizables en la base de datos MNPFren.msi mediante un editor de tablas, como las consultas Orca o SQL.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Localizar columnas de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed36b1adb2c496c9019b482c929e449187b1e0bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082923"
---
# <a name="localizing-database-columns"></a>Localizar columnas de base de datos

Modifique cualquiera de las demás columnas localizables en la base de datos MNPFren.msi mediante un editor de tablas, como las consultas Orca o SQL. Para determinar qué columnas de una tabla determinada se pueden localizar en otro idioma, vea el tema de referencia de la tabla de base de datos. Vea [tablas de base de datos](database-tables.md) para obtener una lista de todas las tablas de base de datos.

Por ejemplo, es posible que el campo de texto de algunos registros de la [tabla de control](control-table.md) deba localizarse en francés. La cadena "¿está seguro de que desea cancelar \[ la \] instalación de ProductName?" en el [cuadro de diálogo cancelar](cancel-dialog.md) se puede modificar en esta tabla para que se muestre en francés. El registro original en el archivo. msi aparece como se indica a continuación.

[Tabla de control](control-table.md) (parcial) del archivo. msi original



| Diálogo\_  | Control | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad | Texto                                                          | Control \_ siguiente | Ayuda |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Texto    | Texto | 48  | 15  | 194   | 30     | 3          |          | ¿Está seguro de que desea cancelar \[ la \] instalación de ProductName? |               |      |



 

Puede usar un editor de tablas para modificar el campo de texto, como el editor de tablas Orca proporcionado con el SDK u otro editor de tablas, o bien usar una consulta SQL para cambiar el campo de texto del registro de la tabla de control. En el SDK de Windows Installer se proporciona un ejemplo en el que se muestran las consultas de base de datos controladas por script como WiRunSQL.vbs de la utilidad. Utilice la siguiente línea de comandos para modificar el campo con WiRunSQL.vbs y Windows Script Host. Vea también [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi "control de conjunto de controles de actualización. Text = ' etes-vous sur de vouloir anulación l'installation de \[ ProductName \] ? ' WHERE control. Dialog \_ = ' CancelDlg ' y control. control = ' texto ' "**

[Tabla de control](control-table.md) (parcial) en MNPFren.msi



| Diálogo\_  | Control | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad | Texto                                                                | Control \_ siguiente | Ayuda |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Texto    | Texto | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sûr vouloir l'installation de \[ NombreProducto \] ? |               |      |



 

Si el usuario cancela la instalación de MNPFren.msi, aparece el cuadro de **diálogo cancelar** que muestra el texto: "êtes-vous sûr de vouloir anulación L'INSTALLATION de MNP2000?"

Al usar este método para localizar el texto de la interfaz de usuario en un idioma diferente, se debe probar la interfaz de usuario localizada para asegurarse de que el tamaño de los controles sea lo suficientemente grande como para mostrar todo el texto localizado. Debe probarse con todos los valores de tamaño de fuente que se pueden mostrar. El texto localizado puede requerir más espacio que el texto original y se puede truncar si se muestra en un control demasiado pequeño.

[Continuar](updating-productlanguage-and-productcode-properties.md)

 

 



