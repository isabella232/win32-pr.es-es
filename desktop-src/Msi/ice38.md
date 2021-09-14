---
description: ICE38 valida que todos los componentes que se instalan en el perfil del usuario actual también especifican una clave del Registro en la raíz HKEY CURRENT USER en la columna KeyPath de la \_ \_ tabla Component.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074616"
---
# <a name="ice38"></a>ICE38

ICE38 valida que todos los componentes que se instalan en el perfil del usuario actual también especifican una clave del Registro en la raíz **HKEY \_ CURRENT \_ USER** de la columna KeyPath de la tabla [Component](component-table.md).

## <a name="result"></a>Resultado

ICE38 publica un error si un componente instalado en el perfil del usuario no especifica una clave del Registro HKCU.

## <a name="example"></a>Ejemplo

ICE38 notifica los siguientes errores para el ejemplo mostrado.



| Error de ICE38                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Componente Component1 se instala en el perfil de usuario. Debe usar una clave del Registro en HKCU como su KeyPath, no como un archivo.                    | El valor de la columna de atributos de Component1 es 0, lo que significa que el componente debe usar un archivo como KeyPath. Esto provoca dificultades cuando varios usuarios instalan el componente en el mismo equipo. Para corregir este error en Component1, establezca el bit RegistryKeyPath en la columna Atributos de la tabla [Component](component-table.md) y cambie la entrada de la columna KeyPath a un valor que aparece en la columna Registro de la tabla [del Registro](registry-table.md).<br/>                                                                                |
| Component Component2 se instala en el perfil de usuario. Debe usar una clave del Registro en HKCU como su KeyPath. KeyPath es actualmente NULL. | Component2 tiene el bit RegistryKeyPath establecido en la columna Atributos de la [tabla Component](component-table.md). Por lo tanto, el campo KeyPath debe contener una clave para la columna Registro de la tabla del [Registro,](registry-table.md) pero la columna KeyPath es Null. Para corregir este error, cambie el valor de KeyPath a una entrada válida en la tabla Registry.<br/>                                                                                                                                                                                                     |
| Componente 3 se instala en el perfil de usuario. Su clave del Registro KeyPath debe estar en HKCU.                                      | Component3 tiene el bit RegistryKeyPath establecido en la columna Atributos de la tabla [Component,](component-table.md) pero la raíz de la entrada del Registro especificada en la columna Raíz de la tabla del Registro especifica **HKEY \_ LOCAL \_ MACHINE** en lugar de **HKEY \_ CURRENT \_ USER**. Para corregir este error, use una entrada del Registro válida en **HKEY \_ LOCAL \_ MACHINE** como KeyPath para este componente o cambie el valor de la columna Raíz de la tabla [del](registry-table.md) Registro a -1 o 1.<br/>                                                                  |
| La entrada del Registro KeyPath para el componente Component4 no existe.                                                                 | Component4 tiene el bit RegistryKeyPath establecido en la columna Atributos de la tabla [Component,](component-table.md) pero la entrada de la columna KeyPath no existe en la [tabla del Registro](registry-table.md). Para corregir este error, agregue una entrada para Reg4 a la tabla del Registro que esté en **HKEY \_ CURRENT \_ USER**.<br/>                                                                                                                                                                                                                                      |
| La entrada del Registro Reg5 se establece como KeyPath para el componente Component5, pero esa entrada del Registro no pertenece a Component5.      | Se encontró la entrada del Registro a la que se hace referencia en la columna KeyPath del componente y se encuentra debajo del árbol HKCU, pero la columna Component de la entrada del Registro no hace referencia al mismo componente que lo indicó como \_ KeyPath. Esto significa que la entrada del Registro utilizada como KeyPath del componente solo se crearía cuando se instalara algún otro componente. Para corregir este error, cambie el valor de KeyPath para hacer referencia a una entrada del Registro que pertenezca al componente o cambie la entrada del Registro para que pertenezca al componente que lo usa como KeyPath.<br/> |



 

[Tabla de directorios](directory-table.md) (parcial)



| Directorio | Elemento primario \_ del directorio | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Directorio\_ | Atributos | KeyPath |
|------------|-------------|------------|---------|
| Componente1 | Dir1        | 0          | Archivo1   |
| Componente 2 | Dir2        | 4          |         |
| Componente 3 | Dir3        | 4          | Reg3    |
| Componente 4 | Dir4        | 4          | Reg4    |
| Componente 5 | Dir5        | 4          | Reg5    |



 

[Tabla del Registro](registry-table.md) (parcial)



| Registro | Root | Value | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Componente 3  |
| Reg5     | 0    |       | Componente 4  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




