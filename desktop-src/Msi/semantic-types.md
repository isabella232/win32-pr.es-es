---
description: Las siguientes entradas en las columnas Format, Type y ContextData de la tabla ModuleConfiguration especifican el tipo semántico de la información que se sustituye en el elemento configurable especificado en la columna Name de esta tabla.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipos semánticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2a0798a9ae7be3c2c0b56483707e3a09f67d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669836"
---
# <a name="semantic-types"></a>Tipos semánticos

Las siguientes entradas en las columnas Format, Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) especifican el tipo semántico de la información que se sustituye en el elemento configurable especificado en la columna Name de esta tabla.

[Tipos de formato de texto](text-format-types.md)



| Formato | Tipo       | ContextData                                                 | Descripción                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Texto   |            |                                                             | Texto arbitrario. Vea [tipo de texto arbitrario](arbitrary-text-type.md).                                        |
| Texto   | Enumeración       | <A>=<a>;<B>=<b>;<C>=<c> | Valor seleccionado de un conjunto. Vea [tipo de enumeración](enum-type.md).                                                 |
| Texto   | Formato  |                                                             | Valor que cumple la definición del texto con formato en el instalador. Vea [tipo con formato](formatted-type.md). |
| Texto   | RTF        |                                                             | Cadena de texto RTF. Vea [tipo RTF](rtf-type.md).                                                          |
| Texto   | Identificador |                                                             | Cadena de texto que se ajusta a un [identificador](identifier.md)de Windows Installer.                              |



 

[Tipos de formato entero](integer-format-types.md)



| Formato  | Tipo | ContextData | Descripción                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Entero |      |             | Un valor entero. Vea [tipo de entero arbitrario](arbitrary-integer-type.md). |



 

[Tipos de formato de clave](key-format-types.md)



| Formato | Tipo      | ContextData      | Descripción                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Clave    | Archivo      | AssemblyContext  | Permite a los usuarios configurar claves externas para los ensamblados de Common Language Runtime o Win32. Consulte [tipo de archivo](file-type.md). |
| Clave    | Binary    | Bitmap           | Clave externa de una fila de tabla binaria que contiene un mapa de bits para su uso en la interfaz de usuario. Vea [Binary Type](binary-type.md).                  |
| Clave    | Binary    | Icono             | Clave externa de una fila de la tabla binaria que contiene un icono para su uso en la interfaz de usuario. Vea [Binary Type](binary-type.md).                   |
| Clave    | Binary    | EXE              | Clave externa de una fila de tabla binaria que contiene un archivo EXE de 32 bits. Vea [Binary Type](binary-type.md).                             |
| Clave    | Binary    | EXE64            | Clave externa de una fila de tabla binaria que contiene un archivo EXE de 32 o 64 bits. Vea [Binary Type](binary-type.md).                       |
| Clave    | Icono      | ShortcutIcon     | Clave externa de una fila de la tabla de iconos que contiene un icono para su uso en un acceso directo. Vea [tipo de icono](icon-type.md).                |
| Clave    | Diálogo    | DialogNext       | Clave externa a una fila de la tabla de diálogo. Vea [tipo de cuadro de diálogo](dialog-type.md).                                                 |
| Clave    | Diálogo    | DialogPrev       | Clave externa a una fila de la tabla de diálogo. Vea [tipo de cuadro de diálogo](dialog-type.md).                                                 |
| Clave    | Directorio | IsolationDir     | Clave externa de una fila de la tabla de directorio en la que pertenecen los archivos aislados. Consulte [tipo de directorio](directory-type.md).            |
| Clave    | Directorio | ShortcutLocation | Clave externa de una fila de la tabla de directorio donde debe instalarse un acceso directo. Consulte [tipo de directorio](directory-type.md).   |
| Clave    | Propiedad  |                  | Clave externa para una fila de propiedad. Vea [tipo de propiedad](property-type.md).                                                 |
| Clave    | Propiedad  | Público           | Clave externa para una fila de propiedad. Vea [tipo de propiedad](property-type.md).                                                 |
| Clave    | Propiedad  | Private          | Clave externa para una fila de propiedad. Vea [tipo de propiedad](property-type.md).                                                 |



 

[Tipos de formato de campo de bits](bitfield-format-types.md)



| Formato   | Tipo | ContextData                                  | Descripción                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Bits |      | <mask>;<A>=<a>;<B> = b | Cambia un subconjunto de bits de una columna. Consulte tipo de campo de [bits arbitrario](arbitrary-bitfield-type.md). |



 

 

 



