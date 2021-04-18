---
description: Siga estas instrucciones para facilitar la localización de Windows Installer paquetes.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparación de un paquete de Windows Installer para la localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652363"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Preparación de un paquete de Windows Installer para la localización

La localización de un paquete de Windows Installer en varios idiomas puede facilitarse enormemente haciendo lo siguiente:

-   Cree una base de datos de instalación básica que tenga una página de códigos neutra. Vea [crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md). La página de códigos de la base de datos localizada se puede establecer importando una tabla de archivo de texto con una página de códigos no neutra en la base de datos base. Vea [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).
-   Organice los archivos que requieren localización en componentes independientes e instálelos en directorios independientes. Esto garantiza que dos paquetes localizados nunca instalan archivos con el mismo nombre en el mismo directorio.

Por ejemplo, una aplicación de todo el mundo que usa los siguientes recursos puede tener tres componentes.



| Componente | Recurso                   |
|-----------|----------------------------|
| WWPN     | worldwide.exe              |
| WWPN     | entradas del registro en todo el mundo |
| WWPN     | acceso directo internacional         |
| ESN       | engui.dll                  |
| ESN       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

Los archivos que deben localizarse se pueden instalar en las siguientes ubicaciones de directorio:

-   \[\] \\worldwide.exe del mundo de ProgramFilesFolder \\
-   \[ProgramFilesFolder \] \\ World \\ English \\engui.dll
-   \[ProgramFilesFolder \] \\ World \\ English \\readme.txt
-   \[\] \\fraui.dll en \\ francés del mundo \\ de ProgramFilesFolder
-   \[\] \\readme.txt en \\ francés del mundo \\ de ProgramFilesFolder

 

 



