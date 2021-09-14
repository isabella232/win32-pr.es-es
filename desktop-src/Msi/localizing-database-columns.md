---
description: Modifique cualquiera de las demás columnas localizables de la base MNPFren.msi datos mediante un editor de tablas como Orca o SQL consultas.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Localización de columnas de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed36b1adb2c496c9019b482c929e449187b1e0bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071944"
---
# <a name="localizing-database-columns"></a>Localización de columnas de base de datos

Modifique cualquiera de las demás columnas localizables de la base MNPFren.msi datos mediante un editor de tablas como Orca o SQL consultas. Para determinar qué columnas de una tabla determinada se pueden localizar a otro idioma, consulte el tema de referencia de esa tabla de base de datos. Vea [Tablas de base de](database-tables.md) datos para obtener una lista de todas las tablas de base de datos.

Por ejemplo, es posible que el campo Texto de algunos registros de la [tabla Control](control-table.md) tenga que traducirse al francés. La cadena "¿Está seguro de que desea cancelar la instalación \[ de \] ProductName?" en el [cuadro de diálogo Cancelar](cancel-dialog.md) se puede modificar en esta tabla para que se muestre en francés. El registro original en .msi archivo aparece como sigue.

[Tabla de](control-table.md) control (parcial) del archivo .msi original



| Diálogo\_  | Control | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad. | Texto                                                          | Control \_ Siguiente | Ayuda |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Texto    | Texto | 48  | 15  | 194   | 30     | 3          |          | ¿Está seguro de que desea cancelar la \[ instalación de \] ProductName? |               |      |



 

Puede usar un editor de tablas para modificar el campo Texto, como el editor de tablas Orca proporcionado con el SDK u otro editor de tablas, o usar una consulta SQL para cambiar el campo Texto del registro de tabla de control. Se proporciona un ejemplo que muestra las consultas de base de datos controladas por scripts en el SDK Windows Installer como la utilidad WiRunSQL.vbs. Use la siguiente línea de comandos para modificar el campo con WiRunSQL.vbs y el host Windows script. Vea también Ejemplos [de consultas de base de datos mediante SQL y Script](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control.Text='Etes-vous sur de vouloir queer l'installation de \[ ProductName \] ?' WHERE Control.Dialog \_ ='CancelDlg' AND Control.Control='Text'"**

[Tabla de](control-table.md) control (parcial) en MNPFren.msi



| Diálogo\_  | Control | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad. | Texto                                                                | Control \_ Siguiente | Ayuda |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Texto    | Texto | 48  | 15  | 194   | 30     | 3          |          | Ötes-vous sör de vouloir queer l'installation de \[ ProductName \] ? |               |      |



 

Si el usuario cancela la instalación de MNPFren.msi, aparece el cuadro de diálogo Cancelar en el que se muestra el texto: "Ötes-vous sör de vouloir displayinger l'installation de MNP2000?" 

Cuando se usa este método para localizar el texto de la interfaz de usuario en un idioma diferente, se debe probar la interfaz de usuario localizada para asegurarse de que el tamaño de los controles es lo suficientemente grande como para mostrar todo el texto localizado. Debe probarse con todas las configuraciones de tamaño de fuente que están disponibles para mostrarse. El texto localizado puede requerir más espacio que el texto original y puede truncarse si se muestra en un control demasiado pequeño.

[Continuar](updating-productlanguage-and-productcode-properties.md)

 

 



