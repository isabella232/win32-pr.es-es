---
description: La función RegOpenUserClassesRoot proporciona una vista combinada para los procesos, como los servicios, que se ocupan de los clientes que no son el usuario interactivo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Vista combinada de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668445"
---
# <a name="merged-view-of-hkey_classes_root"></a>Vista combinada de la \_ raíz de las clases HKEY \_

La función [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) proporciona una vista combinada para los procesos, como los servicios, que se ocupan de los clientes que no son el usuario interactivo. En este caso, la **clave \_ \_ raíz de las clases HKEY** proporciona una vista del registro que combina la información de **\_ \_ \\ \\ las clases de software del equipo local HKEY** con la información de **\_ \_ \\ \\ las clases de software de usuario actuales de HKEY**.

El sistema utiliza las siguientes reglas para combinar información de los dos orígenes:

-   La vista combinada incluye todas las subclaves de la clave **HKEY \_ Current \_ User \\ \\ classes** .
-   La vista combinada incluye todas las subclaves inmediatas de la clave **HKEY \_ local \_ Machine \\ software \\ classes** que no duplican las subclaves de **\_ \_ \\ \\ las clases de software de usuario actuales de HKEY**.
-   Al final de este tema encontrará una lista de las subclaves que se encuentran en las clases **HKEY \_ local \_ Machine \\ software \\ classes** y **HKEY \_ Current \_ User \\ \\ classes**. Las subclaves inmediatas de estas claves del árbol de **\_ \_ máquina local HKEY** solo se incluyen en la vista combinada si no son duplicados de subclaves inmediatas del árbol de **\_ \_ usuarios actual de HKEY** . La vista combinada no incluye el contenido de **la \_ \_ máquina local HKEY** de las subclaves duplicadas.

Si una aplicación se ejecuta con derechos de administrador y el control de cuentas de usuario está deshabilitado, el tiempo de ejecución de COM omite la configuración de COM por usuario y solo tiene acceso a la configuración COM por equipo. Las aplicaciones que requieren derechos de administrador deben registrar objetos COM dependientes durante la instalación en el almacén de configuración COM por equipo (**\_ clases de \_ \\ software \\ de máquina local HKEY**). Para obtener más información, vea [AC: UAC: COM Per-User configuración](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 y Windows XP/2000:** Las aplicaciones pueden registrar objetos COM dependientes en el almacén de configuración COM por equipo o por usuario **( \_ \_ clases de \\ software \\ de máquina local HKEY** o **\_ \_ \\ \\ clases de software de usuario actual HKEY**).

En el ejemplo siguiente se muestra un conjunto de subclaves de la **\_ \_ máquina local HKEY** y las claves de **\_ \_ usuario actuales HKEY** y la vista combinada resultante de **\_ las clases HKEY \_ root**.

**HKEY \_ \_Clases de \\ software \\ de máquina local**    **CLSID**       *2*       *4*          **InProcServer32**          **LocalServer32**       *7*

**HKEY \_ \_Clases de \\ software \\ de usuario actual**    **CLSID**       *1*       *4*          **LocalServer**       *6*       *10*          **LocalServer**

**HKEY \_ El CLSID \_ raíz de clases***1**2**4***InProcServer32****LocalServer** de **LocalServer32***6**7**10***LocalServer**                                                                                      

Las siguientes subclaves se encuentran en las clases **HKEY \_ local \_ Machine \\ software \\ classes** y **HKEY \_ Current \_ User \\ software \\ classes**. En el árbol de **\_ \_ máquina local HKEY** , las subclaves inmediatas de estas claves se incluyen en la vista combinada solo si no son duplicados de las subclaves inmediatas del árbol de **\_ \_ usuarios actual de HKEY** . La vista combinada no incluye el contenido de **la \_ \_ máquina local HKEY** de las subclaves duplicadas.

**\**_ _*\*\\ shellex**  
**\*\\shellex \\ ContextMenuHandlers**  
**\*\\shellex \\ PropertySheetHandlers**  
**AppID**  
**ClsID**  
**Categorías del componente**  
**Unidad**  
**Shellex de unidad \\**  
**Unidad \\ shellex \\ ContextMenuHandlers**  
**Unidad \\ shellex \\ PropertySheetHandlers**  
**FileType**  
**Carpeta**  
**Carpeta \\ shellex**  
**Carpeta \\ shellex \\ ColumnHandler**  
**Carpeta \\ shellex \\ ContextMenuHandlers**  
**Carpeta \\ shellex \\ ExtShellFolderViews**  
**Carpeta \\ shellex \\ PropertySheetHandlers**  
**Componentes del instalador \\**  
**Características del instalador \\**  
**Productos de instalador \\**  
**Interfaz**  
**Mine**  
**\\Base de datos MIME**  
**\\Juego de caracteres de base de datos MIME \\**  
**\\Página de códigos de base de datos MIME \\**  
**\\Tipo de contenido de base de datos MIME \\**  
**Typelib**  


 

 
