---
description: Las siguientes entradas de las columnas Format, Type y ContextData de la tabla ModuleConfiguration especifican el tipo semántico de información que se sustituye en el elemento configurable especificado en la columna Nombre de esta tabla.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipos semánticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01845bd7790f618794816182bb4b11fc0d13baf9216d17bbd15c63a390a52a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040305"
---
# <a name="semantic-types"></a>Tipos semánticos

Las siguientes entradas de las columnas Format, Type y ContextData de la tabla [ModuleConfiguration](moduleconfiguration-table.md) especifican el tipo semántico de información que se sustituye en el elemento configurable especificado en la columna Nombre de esta tabla.

[Tipos de formato de texto](text-format-types.md)



| Formato | Tipo       | ContextData                                                 | Descripción                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Texto   |            |                                                             | Texto arbitrario. Vea [Tipo de texto arbitrario.](arbitrary-text-type.md)                                        |
| Texto   | Enumeración       | <A>=<a>;<B>=<b>;<C>=<c> | Valor seleccionado de un conjunto. Vea [Tipo de enumeración](enum-type.md).                                                 |
| Texto   | Formato  |                                                             | Valor que reúne la definición de Texto con formato en el instalador. Vea [Tipo con formato](formatted-type.md). |
| Texto   | RTF        |                                                             | Cadena de texto RTF. Vea [tipo RTF](rtf-type.md).                                                          |
| Texto   | Identificador |                                                             | Cadena de texto que se ajusta a un Windows identificador del [instalador](identifier.md).                              |



 

[Tipos de formato entero](integer-format-types.md)



| Formato  | Tipo | ContextData | Descripción                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Entero |      |             | Un valor entero. Vea [Tipo entero arbitrario](arbitrary-integer-type.md). |



 

[Tipos de formato de clave](key-format-types.md)



| Formato | Tipo      | ContextData      | Descripción                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Clave    | Archivo      | AssemblyContext  | Permitir que los usuarios configuren claves externas en ensamblados de Win32 o Common Language Runtime. Vea [Tipo de archivo](file-type.md). |
| Clave    | Binary    | Bitmap           | Clave externa a una fila de tabla binaria que contiene un mapa de bits para su uso en la interfaz de usuario. Vea [Tipo binario](binary-type.md).                  |
| Clave    | Binary    | Icono             | Clave externa a una fila de tabla binaria que contiene un icono para su uso en la interfaz de usuario. Vea [Tipo binario](binary-type.md).                   |
| Clave    | Binary    | EXE              | Clave externa a una fila de tabla binaria que contiene un archivo EXE de 32 bits. Vea [Tipo binario](binary-type.md).                             |
| Clave    | Binary    | EXE64            | Clave externa a una fila de tabla binaria que contiene un exe de 32 o 64 bits. Vea [Tipo binario](binary-type.md).                       |
| Clave    | Icono      | ShortcutIcon     | Tecla externa a una fila de la tabla Icono que contiene un icono para su uso mediante un acceso directo. Vea [Icon Type (Tipo de icono).](icon-type.md)                |
| Clave    | Diálogo    | DiálogoSiguiente       | Clave externa a una fila de tabla dialog. Vea [Tipo de diálogo](dialog-type.md).                                                 |
| Clave    | Diálogo    | DialogPrev       | Clave externa a una fila de tabla dialog. Vea [Tipo de diálogo](dialog-type.md).                                                 |
| Clave    | Directorio | IsolationDir     | Clave externa a una fila de la tabla Directory a la que pertenecen los archivos aislados. Vea [Tipo de directorio](directory-type.md).            |
| Clave    | Directorio | ShortcutLocation | Clave externa a una fila de la tabla Directory donde se debe instalar un acceso directo. Vea [Tipo de directorio](directory-type.md).   |
| Clave    | Propiedad  |                  | Clave externa a una fila de propiedad. Vea [Tipo de propiedad](property-type.md).                                                 |
| Clave    | Propiedad  | Público           | Clave externa a una fila de propiedad. Vea [Tipo de propiedad](property-type.md).                                                 |
| Clave    | Propiedad  | Privada          | Clave externa a una fila de propiedad. Vea [Tipo de propiedad](property-type.md).                                                 |



 

[Tipos de formato de campo de bits](bitfield-format-types.md)



| Formato   | Tipo | ContextData                                  | Descripción                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Campo de bits |      | <mask>;<A>=<a>;<B> =b | Cambia un subconjunto de bits de una columna. Vea [Tipo de campo de bits arbitrario.](arbitrary-bitfield-type.md) |



 

 

 



