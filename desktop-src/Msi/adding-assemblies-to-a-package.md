---
description: Windows Los desarrolladores de instaladores pueden usar las directrices de este tema para crear Windows installer que contienen ensamblados.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Agregar ensamblados a un paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159217"
---
# <a name="adding-assemblies-to-a-package"></a>Agregar ensamblados a un paquete

Windows Los desarrolladores de instaladores pueden usar las directrices de este tema para crear Windows installer que contienen ensamblados.

Las siguientes directrices se aplican a los ensamblados win32 y a los ensamblados que common language runtime de microsoft .NET Framework usa.

-   Un Windows installer no debe contener más de un ensamblado.
-   Todos los archivos del ensamblado deben estar en un solo componente.
-   Cada componente que contiene un ensamblado debe tener una entrada en la [tabla MsiAssembly.](msiassembly-table.md)
-   El nombre de caché de ensamblados segura de cada ensamblado debe crearse en la [tabla MsiAssemblyName.](msiassemblyname-table.md)
-   Use la [tabla Registry](registry-table.md) en lugar de la [tabla Class](class-table.md) al registrar la interoperabilidad COM para un ensamblado.
-   Los ensamblados que tienen el mismo nombre de seguridad son el mismo ensamblado. Cuando diferentes aplicaciones instalan el mismo ensamblado, los componentes que contienen el ensamblado deben usar el mismo valor para ComponentId en sus [tablas component.](component-table.md)

> [!Note]  
> Los anuncios de productos identifican los ensamblados que se pueden instalar y usar en distintas aplicaciones. Los anuncios de productos no identifican ensamblados privados.

 

## <a name="adding-win32-assemblies"></a>Agregar ensamblados win32

Use las siguientes directrices al incluir ensamblados win32:

-   El valor de KeyPath de la [tabla Component](component-table.md) de un componente que contiene un ensamblado Win32 no debe ser Null.
-   El valor keyPath de la [tabla Component](component-table.md) de un componente que contiene un ensamblado de directiva Win32 debe ser el archivo de manifiesto.
-   El valor KeyPath de la tabla [Component](component-table.md) de un componente que contiene un ensamblado Win32, que no es un ensamblado de directiva, no debe ser el archivo de manifiesto o el archivo de catálogo. Debe ser un archivo diferente en el ensamblado.
-   Agregue una fila a la [tabla MsiAssemblyName](msiassemblyname-table.md) para cada par de nombre y valor que se enumeran en la sección **assemblyIdentity** del manifiesto del ensamblado Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Agregar ensamblados usados con el .NET Framework

Use las siguientes directrices al incluir ensamblados que common language runtime del .NET Framework utiliza.

-   El valor de KeyPath de la [tabla Component](component-table.md) de un componente que contiene el ensamblado no debe ser Null.
-   Al instalar un ensamblado usado por Common Language Runtime en la caché global de ensamblados, el valor de la columna Aplicación de archivo de la \_ tabla MsiAssembly debe ser Null.
-   Agregue una fila a la [tabla MsiAssemblyName](msiassemblyname-table.md) para cada atributo del nombre de seguridad del ensamblado. Todos los ensamblados deben tener los atributos Name, Version y Culture que se especifican en la tabla MsiAssemblyName. Se requiere un atributo publicKeyToken para un ensamblado global. La tabla siguiente es un ejemplo de la tabla MsiAssemblyName para un ensamblado global para su uso por Common Language Runtime.

[Tabla MsiAssemblyName](msiassemblyname-table.md)



| Componente  | Nombre           | Value            |
|------------|----------------|------------------|
| ComponenteA | Nombre           | simple           |
| ComponenteA | version        | 1.0.0.0          |
| ComponenteA | culture        | neutral          |
| ComponenteA | Publickeytoken | 9d1ec8380f483f5a |



 

 

 



