---
description: La función RegOpenUserClassesRoot proporciona una vista combinada para los procesos, como los servicios, que están tratando con clientes distintos del usuario interactivo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Vista combinada de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371887"
---
# <a name="merged-view-of-hkey_classes_root"></a>Vista combinada de HKEY \_ CLASSES \_ ROOT

La [**función RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) proporciona una vista combinada para los procesos, como los servicios, que están tratando con clientes distintos del usuario interactivo. En este caso, la clave RAÍZ **HKEY \_ \_ CLASSES** proporciona una vista del Registro que combina la información de **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes** con la información de **HKEY CURRENT USER \_ Software \_ \\ \\ Classes**.

El sistema usa las siguientes reglas para combinar información de los dos orígenes:

-   La vista combinada incluye todas las subclaves de la clave **HKEY \_ CURRENT USER \_ Software \\ \\ Classes.**
-   La vista combinada incluye todas las subclaves inmediatas de la clave **HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** que no duplican las subclaves de las clases de **software HKEY CURRENT \_ \_ USER \\ \\**.
-   Al final de este tema se muestra una lista de subclaves que se encuentran en las clases de **software HKEY \_ LOCAL MACHINE \_ \\ y \\** **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. Las subclaves inmediatas de estas claves del árbol **HKEY \_ LOCAL \_ MACHINE** solo se incluyen en la vista combinada si no son duplicados de subclaves inmediatas del árbol **HKEY \_ CURRENT \_ USER.** La vista combinada no incluye el contenido **de HKEY \_ LOCAL \_ MACHINE** de subclaves duplicadas.

Si una aplicación se ejecuta con derechos de administrador y el control de cuentas de usuario está deshabilitado, el tiempo de ejecución com omite la configuración COM por usuario y solo tiene acceso a la configuración COM por equipo. Las aplicaciones que requieren derechos de administrador deben registrar objetos COM dependientes durante la instalación en el almacén de configuración COM por máquina ( clases de **software HKEY \_ LOCAL \_ MACHINE \\ \\**). Para obtener más información, [vea AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 y Windows XP/2000:** Las aplicaciones pueden registrar objetos COM dependientes en el almacén de configuración COM por equipo o por usuario ( clases de **software HKEY \_ LOCAL \_ MACHINE \\ \\** o clases de **software HKEY \_ CURRENT \_ USER \\ \\**).

En el ejemplo siguiente se muestra un conjunto de subclaves en las claves **HKEY \_ LOCAL \_ MACHINE** y **HKEY \_ CURRENT \_ USER** y la vista combinada resultante de **HKEY CLASSES \_ \_ ROOT**.

**HKEY \_ Clases \_ \\ DE SOFTWARE \\ DE** MÁQUINA LOCAL **CLSID***2**4***inprocserver32****localserver32***7*                                             

**HKEY \_ Clases \_ \\ de software DE \\ USUARIO**    **ACTUAL CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**

**HKEY \_ CLASSES \_ ROOT**    **CLSID**       *1*       *2*       *4*          **inprocserver32**          **localserver**          **localserver32**       *6*       *7*       *10*          **localserver**

Las subclaves siguientes se encuentran en las clases de **software HKEY \_ LOCAL MACHINE \_ \\ y \\** **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. Desde el árbol **HKEY \_ LOCAL \_ MACHINE,** las subclaves inmediatas de estas claves se incluyen en la vista combinada solo si no son duplicados de subclaves inmediatas del árbol **HKEY \_ CURRENT \_ USER.** La vista combinada no incluye el contenido **de HKEY \_ LOCAL \_ MACHINE** de subclaves duplicadas.

**\***  
**\*\\shellex**  
**\*\\shellex \\ ContextMenuHandlers**  
**\*\\shellex \\ PropertySheetHandlers**  
**AppID**  
**Clsid**  
**Categorías del componente**  
**Unidad**  
**Shellex \\ de unidad**  
**Unidad \\ \\ contextMenuHandlers de shellex**  
**Unidad \\ shellex \\ PropertySheetHandlers**  
**FileType**  
**Carpeta**  
**Shellex \\ de carpeta**  
**Folder \\ shellex \\ ColumnHandler**  
**\\ \\ ContextMenuHandlers de shell de carpetas**  
**Shellex \\ de \\ carpeta ExtShellFolderViews**  
**\\ \\ PropertySheetHandlers de shell de carpetas**  
**Componentes del \\ instalador**  
**Características del \\ instalador**  
**Productos del \\ instalador**  
**Interfaz**  
**Mime**  
**Base de \\ datos Mime**  
**Juego \\ de caracteres de base de datos \\ Mime**  
**Mime \\ Database \\ Codepage**  
**Tipo \\ de contenido de base de datos \\ Mime**  
**Typelib**  


 

 
