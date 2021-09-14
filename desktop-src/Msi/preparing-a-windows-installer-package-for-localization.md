---
description: Siga estas directrices para facilitar la localización de paquetes Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparar un paquete Windows instalador para la localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161455"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Preparar un paquete Windows instalador para la localización

La localización de un paquete Windows Installer en varios idiomas se puede facilitar enormemente haciendo lo siguiente:

-   Cree una base de datos de instalación base que sea neutra en la página de códigos. Consulte [Creación de una base de datos con una página de códigos neutra.](creating-a-database-with-a-neutral-code-page.md) La página de códigos de la base de datos localizada se puede establecer importando una tabla de archivo de texto con una página de códigos no neutra en la base de datos base. Vea [Establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).
-   Organice los archivos que requieren localización en componentes independientes e instale estos archivos en directorios independientes. Esto garantiza que dos paquetes localizados nunca instalen archivos con el mismo nombre en el mismo directorio.

Por ejemplo, una aplicación mundial que usa los siguientes recursos puede tener tres componentes.



| Componente | Recurso                   |
|-----------|----------------------------|
| MUNDO     | worldwide.exe              |
| MUNDO     | entradas del Registro en todo el mundo |
| MUNDO     | acceso directo en todo el mundo         |
| ESN       | engui.dll                  |
| ESN       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

Los archivos que deben localizarse pueden instalarse en las siguientes ubicaciones de directorio:

-   \[ProgramFilesFolder \] \\ World \\worldwide.exe
-   \[ProgramFilesFolder \] \\ World English \\ \\engui.dll
-   \[ProgramFilesFolder \] \\ World English \\ \\readme.txt
-   \[ProgramFilesFolder \] \\ World French \\ \\fraui.dll
-   \[ProgramFilesFolder \] \\ World French \\ \\readme.txt

 

 



