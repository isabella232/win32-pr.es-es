---
description: ICE50 comprueba que se especifican los iconos de acceso directo para que se muestren correctamente y coincidan con la extensión del archivo de destino.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002562"
---
# <a name="ice50"></a>ICE50

ICE50 comprueba que se especifican los iconos de acceso directo para que se muestren correctamente y coincidan con la extensión del archivo de destino.

## <a name="result"></a>Resultado

ICE50 envía un mensaje de error si la extensión del icono y los archivos de destino no coinciden. ICE50 publica una advertencia si los iconos se almacenan en archivos que no tienen una extensión. exe o. ico.

## <a name="example"></a>Ejemplo

ICE50 notifica el siguiente error para el ejemplo que se muestra.



| Error o advertencia de ICE50                                                                                                              | Descripción                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La extensión del icono ' Icon2. dat ' para el acceso directo ' Shortcut2 ' no coincide con la extensión del archivo de clave del componente ' Component2 '. | Si las extensiones del icono y del archivo de destino no coinciden, el acceso directo no tendrá el menú contextual correcto cuando se anuncie el componente. Para corregir este error, cambie el nombre del icono para que coincida con la extensión del archivo de destino.<br/> |
| La extensión del icono ' Icon1.bat ' para el acceso directo ' Shortcut1 ' no es ' exe ' ni ' ico '. El icono no se mostrará correctamente.         | No todas las versiones del shell muestran correctamente los iconos almacenados en archivos que no tienen extensiones de "exe" o "ICO". Para corregir esta advertencia, cambie el nombre del icono por la extensión "exe" o "ICO".<br/>                                      |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | FileName  |
|-------|-----------|
| Archivo1 | File1.bat |
| Archivo2 | File2.pl  |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  |
|----------|
| Feature1 |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Rutas |
|------------|---------|
| Component1 | Archivo1   |
| Component2 | Archivo2   |



 

[Tabla de iconos](icon-table.md)



| Nombre      | Datos            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icon2. dat | \[Binary Data\] |



 

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Componente  | Destino   | Icono\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Component1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2. dat |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




