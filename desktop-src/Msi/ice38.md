---
description: ICE38 valida que todos los componentes que se instalan en el perfil del usuario actual también especifican una clave del registro en la \_ \_ raíz de usuario actual de HKEY en la columna de ruta de clave de la tabla de componentes.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082925"
---
# <a name="ice38"></a>ICE38

ICE38 valida que todos los componentes que se instalan en el perfil del usuario actual también especifican una clave del registro en la raíz de **\_ \_ usuario actual de HKEY** en la columna de ruta de clave de la [tabla de componentes](component-table.md).

## <a name="result"></a>Resultado

ICE38 publica un error si un componente instalado en el perfil del usuario no especifica una clave del registro HKCU.

## <a name="example"></a>Ejemplo

ICE38 notifica los siguientes errores para el ejemplo mostrado.



| Error ICE38                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El componente Component1 se instala en el perfil de usuario. Debe usar una clave del registro en HKCU como su ruta de acceso, no un archivo.                    | El valor de la columna Attributes de Component1 es 0, lo que significa que el componente debe usar un archivo como su ruta de acceso. Esto produce dificultades cuando varios usuarios instalan el componente en el mismo equipo. Para corregir este error en Component1, establezca el bit RegistryKeyPath en la columna atributos de la [tabla componente](component-table.md) y cambie la entrada en la columna ruta de acceso de la clave a un valor que aparece en la columna registro de la [tabla del registro](registry-table.md).<br/>                                                                                |
| El componente Component2 se instala en el perfil de usuario. Debe usar una clave del registro en HKCU como su ruta de clave. La ruta de la ruta de la ruta es actualmente NULL. | Component2 tiene el bit RegistryKeyPath establecido en la columna Attributes de la [tabla Component](component-table.md). Por tanto, el campo de ruta de clave debe contener una clave para la columna del registro de la [tabla del registro](registry-table.md) , pero la columna de ruta de clave es NULL. Para corregir este error, cambie el valor de la ruta de clave a una entrada válida en la tabla del registro.<br/>                                                                                                                                                                                                     |
| El componente Component3 se instala en el perfil de usuario. La clave del registro de la ruta de claves debe estar en HKCU.                                      | Component3 tiene el bit RegistryKeyPath establecido en la columna Attributes de la [tabla Component](component-table.md) , pero la raíz de la entrada del registro especificada en la columna root de la tabla Registry especifica el **\_ \_ equipo local HKEY** en lugar de **HKEY \_ Current \_ User**. Para corregir este error, use una entrada del registro válida en **HKEY \_ local \_ Machine** como la ruta de acceso clave de este componente o cambie el valor de la columna raíz de la [tabla del registro](registry-table.md) a-1 o 1.<br/>                                                                  |
| La entrada del registro de la ruta de acceso del componente Component4 no existe.                                                                 | Component4 tiene el bit RegistryKeyPath establecido en la columna Attributes de la [tabla Component](component-table.md) , pero la entrada de la columna de ruta de clave no existe en la [tabla del registro](registry-table.md). Para corregir este error, agregue una entrada para Reg4 a la tabla del registro que se encuentra en **HKEY \_ Current \_ User**.<br/>                                                                                                                                                                                                                                      |
| La entrada del registro Reg5 se establece como la ruta de acceso clave para el componente Component5, pero esa entrada del registro no pertenece a Component5.      | Se encontró la entrada del registro a la que se hace referencia en la columna de clave de ruta de acceso del componente y se encuentra en el árbol HKCU, pero la columna de componente de la entrada del registro \_ no hace referencia al mismo componente que la ha mostrado como ruta de acceso clave. Esto significa que la entrada del registro utilizada como ruta de acceso del componente solo se crearía cuando se instalara algún otro componente. Para corregir este error, cambie el valor de la ruta de acceso para hacer referencia a una entrada del registro que pertenezca al componente o cambie la entrada del registro para que pertenezca al componente que la usa como una ruta de acceso clave.<br/> |



 

[Tabla de directorio](directory-table.md) (parcial)



| Directorio | Directorio \_ primario | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Directorio\_ | Atributos | Rutas |
|------------|-------------|------------|---------|
| Component1 | Dir1        | 0          | Archivo1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

[Tabla del registro](registry-table.md) (parcial)



| Registro | Root | Value | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




