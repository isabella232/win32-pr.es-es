---
description: ICE50 comprueba que los iconos de acceso directo se especifican para que se muestren correctamente y coincidan con la extensión del archivo de destino.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074591"
---
# <a name="ice50"></a>ICE50

ICE50 comprueba que los iconos de acceso directo se especifican para que se muestren correctamente y coincidan con la extensión del archivo de destino.

## <a name="result"></a>Resultado

ICE50 publica un mensaje de error si la extensión del icono y los archivos de destino no coinciden. ICE50 envía una advertencia si los iconos se almacenan en archivos que no tienen una extensión .exe o .ico.

## <a name="example"></a>Ejemplo

ICE50 notifica el siguiente error para el ejemplo mostrado.



| Error o advertencia de ICE50                                                                                                              | Descripción                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La extensión del icono "Icon2.dat" para el acceso directo "Shortcut2" no coincide con la extensión del archivo de claves para el componente "Component2". | Si las extensiones del icono y el archivo de destino no coinciden, el acceso directo no tendrá el menú contextual correcto cuando se anuncie el componente. Para corregir este error, cambie el nombre del icono para que coincida con la extensión del archivo de destino.<br/> |
| La extensión del icono "Icon1.bat" para el acceso directo "Shortcut1" no es "exe" ni "ico". El icono no se mostrará correctamente.         | No todas las versiones del shell muestran correctamente iconos almacenados en archivos que no tienen extensiones de "exe" o "ico". Para corregir esta advertencia, cambie el nombre del icono por una extensión de "exe" o "ico".<br/>                                      |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | FileName  |
|-------|-----------|
| Archivo1 | File1.bat |
| Archivo2 | File2.pl  |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  |
|----------|
| Característica 1 |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | KeyPath |
|------------|---------|
| Componente1 | Archivo1   |
| Componente 2 | Archivo2   |



 

[Tabla de iconos](icon-table.md)



| Nombre      | Datos            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icono2.dat | \[Binary Data\] |



 

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Componente  | Destino   | Icono\_    |
|-----------|------------|----------|-----------|
| Acceso directo1 | Componente1 | Característica 1 | Icon1.bat |
| Acceso directo2 | Componente 2 | Característica 1 | Icono2.dat |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




