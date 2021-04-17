---
description: ICE62 realiza comprobaciones exhaustivas en la tabla IsolatedComponent para los datos que pueden provocar un comportamiento inesperado.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667941"
---
# <a name="ice62"></a>ICE62

ICE62 realiza comprobaciones exhaustivas en la [tabla IsolatedComponent](isolatedcomponent-table.md) para los datos que pueden provocar un comportamiento inesperado.

Si no se corrige un error detectado por ICE62, puede producirse un error en el sistema de componentes aislados en una gran variedad de formas. Por ejemplo, si no se establece el bit SharedDllRefCount para un componente compartido, el registro del componente podría quitarse cuando otra aplicación utiliza ese ComponentId y se desinstala.

## <a name="result"></a>Resultado

ICE62 publica una advertencia o un error cuando encuentra datos en la tabla IsolatedComponent que pueden producir un comportamiento inesperado.

## <a name="example"></a>Ejemplo

ICE62 notifica los siguientes errores y advertencias para los ejemplos que se muestran.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 aparece como componente de la aplicación para el aislamiento de component1. Sin embargo, Component2 tiene una ruta de acceso de clave del registro y no proporciona una ruta de acceso ejecutable válida que se pueda usar para aislar el componente.

Para corregir este error, use otro componente como la aplicación del componente de modo aislado component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 aparece como un componente compartido aislado, pero no tiene establecido el bit SharedDllRefCount. Esto podría dar lugar a que la duración del componente sea incorrecta. Si otra aplicación utiliza este componente (aislado o no) y se desinstala, el registro del componente se quita pero la copia aislada de la aplicación permanece. Esto provoca problemas de reparación y desinstalación.

Para corregir este error, establezca el bit SharedDllRefCount para el componente.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 y Component2 se instalan con características diferentes. Component1 se instala mediante Feature1 y Component2 se instala mediante Característica2. Feature1 no es un elemento primario de Característica2, por lo que es posible que la aplicación se instale, pero no el componente aislado, lo que interrumpe el aislamiento.

Para corregir este error, agregue una entrada a la tabla FeatureComponents vinculando Component1 a la misma característica que (o una característica primaria de) la característica que instala Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 tiene una condición en la tabla de componentes. Si alguna vez cambia la condición de TRUE a FALSE durante la vigencia de una instalación en un equipo, el componente aislado podría quedar huérfano sin información de registro.

Para corregir esta advertencia, quite la condición o cree la condición para que nunca pueda cambiar de TRUE a FALSE.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 está aislado para Component2 y Component3, y los dos componentes también se instalan en el mismo directorio. Las aplicaciones comparten un componente aislado, pero si se quita una aplicación, se quita el componente compartido, lo que hace que las demás aplicaciones pierdan el componente aislado.

Para corregir esta advertencia, instale las aplicaciones en directorios diferentes o Compruebe si algunas de las aplicaciones requieren realmente un componente aislado.

[Tabla IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ compartido | Aplicación de componentes \_ |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[Tabla de componentes](component-table.md)



| Componente  | ComponentId | Directorio\_ | Atributos | Condición   | Rutas   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | Mi condición | Archivo1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | File3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Característica2  | Component2  |
| Feature1  | Component3  |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  | Característica \_ principal |
|----------|-----------------|
| Feature1 |                 |
| Característica2 |                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



