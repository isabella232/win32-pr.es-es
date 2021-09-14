---
description: Las siguientes entradas de las columnas Format, Type y ContextData de la tabla ModuleConfiguration especifican el tipo semántico de información que se sustituye en el elemento configurable especificado en la columna Nombre de esta tabla.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipos semánticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234e5dd929991c2ec5fecbc1d2d1bda72f4fbe52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260975"
---
# <a name="semantic-types"></a>Tipos semánticos

Las siguientes entradas de las columnas Format, Type y ContextData de la tabla [ModuleConfiguration](moduleconfiguration-table.md) especifican el tipo semántico de información que se sustituye en el elemento configurable especificado en la columna Nombre de esta tabla.

[Tipos de formato de texto](text-format-types.md)



| Formato | Tipo       | ContextData                                                 | Descripción                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Texto   |            |                                                             | Texto arbitrario. Vea [Tipo de texto arbitrario](arbitrary-text-type.md).                                        |
| Texto   | Enumeración       | <A>=<a>;<B>=<b>;&lt; C &gt; = &lt; c&gt; | Valor seleccionado de un conjunto. Vea [Tipo de enumeración](enum-type.md).                                                 |
| Texto   | Formato  |                                                             | Valor que se encuentra en la definición de Texto con formato en el instalador. Vea [Tipo con formato](formatted-type.md). |
| Texto   | RTF        |                                                             | Cadena de texto RTF. Vea [RTF Type (Tipo RTF).](rtf-type.md)                                                          |
| Texto   | Identificador |                                                             | Cadena de texto que se ajusta a un Windows identificador del [instalador](identifier.md).                              |



 

[Tipos de formato entero](integer-format-types.md)



| Formato  | Tipo | ContextData | Descripción                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Entero |      |             | Un valor entero. Vea [Tipo entero arbitrario](arbitrary-integer-type.md). |



 

[Tipos de formato de clave](key-format-types.md)



| Formato | Tipo      | ContextData      | Descripción                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Clave    | Archivo      | AssemblyContext  | Permitir a los usuarios configurar claves externas en ensamblados de Win32 o Common Language Runtime. Vea [Tipo de archivo](file-type.md). |
| Clave    | Binary    | Bitmap           | Clave externa para una fila de tabla binaria que contiene un mapa de bits para su uso en la interfaz de usuario. Vea [Tipo binario](binary-type.md).                  |
| Clave    | Binary    | Icono             | Clave externa a una fila de tabla binaria que contiene un icono para su uso en la interfaz de usuario. Vea [Tipo binario](binary-type.md).                   |
| Clave    | Binary    | EXE              | Clave externa para una fila de tabla binaria que contiene un exe de 32 bits. Vea [Tipo binario](binary-type.md).                             |
| Clave    | Binary    | EXE64            | Clave externa a una fila de tabla binaria que contiene un exe de 32 o 64 bits. Vea [Tipo binario](binary-type.md).                       |
| Clave    | Icono      | ShortcutIcon     | Tecla externa para una fila de tabla icono que contiene un icono para su uso mediante un acceso directo. Vea [Icon Type (Tipo de icono).](icon-type.md)                |
| Clave    | Diálogo    | Cuadro de diálogoSiguiente       | Clave externa a una fila de tabla dialog. Vea [Tipo de cuadro de diálogo](dialog-type.md).                                                 |
| Clave    | Diálogo    | DialogPrev       | Clave externa a una fila de tabla dialog. Vea [Tipo de cuadro de diálogo](dialog-type.md).                                                 |
| Clave    | Directorio | IsolationDir     | Clave externa a una fila de la tabla Directory a la que pertenecen los archivos aislados. Vea [Tipo de directorio](directory-type.md).            |
| Clave    | Directorio | ShortcutLocation | Clave externa a una fila de la tabla Directory donde se debe instalar un acceso directo. Vea [Tipo de directorio](directory-type.md).   |
| Clave    | Propiedad  |                  | Clave externa a una fila de propiedad. Vea [Tipo de propiedad](property-type.md).                                                 |
| Clave    | Propiedad  | Público           | Clave externa a una fila de propiedad. Vea [Tipo de propiedad](property-type.md).                                                 |
| Clave    | Propiedad  | Privada          | Clave externa a una fila de propiedad. Vea [Tipo de propiedad](property-type.md).                                                 |



 

[Tipos de formato de campo de bits](bitfield-format-types.md)



| Formato   | Tipo | ContextData                                  | Descripción                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Campo de bits |      | &lt;mask &gt; ; <A> = <a> ; <B> =b | Cambia un subconjunto de bits de una columna. Vea [Tipo de campo de bits arbitrario.](arbitrary-bitfield-type.md) |



 

 

 



