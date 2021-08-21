---
description: La tabla TypeLib contiene la información que debe colocarse en el registro de bibliotecas de tipos.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabla TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862bc37e325f8c615e8158cfa431c927841f6b33c403c804726cea8fee6f0469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500005"
---
# <a name="typelib-table"></a>Tabla TypeLib

La tabla TypeLib contiene la información que debe colocarse en el registro de bibliotecas de tipos.

La tabla TypeLib tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
|-------------|------------------------------------|-----|----------|
| LibID       | [GUID](guid.md)                   | Y   | N        |
| Lenguaje    | [Entero](integer.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md)       | Y   | N        |
| Versión     | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Descripción | [Texto](text.md)                   | N   | Y        |
| Directorio\_ | [Identificador](identifier.md)       | N   | Y        |
| Característica\_   | [Identificador](identifier.md)       | N   | N        |
| Costo        | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID
</dt> <dd>

GUID que identifica la biblioteca.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lengua
</dt> <dd>

Idioma de la biblioteca de tipos. Debe ser un número no negativo.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md). Esta columna identifica el componente que pertenece a Feature \_ cuyo archivo de clave es la biblioteca de tipos que se está registrando.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versión
</dt> <dd>

Esta es la versión de la biblioteca. Las versiones principal y secundaria se codifican en el valor entero de cuatro bytes. La versión secundaria está en los ocho bits inferiores. La versión principal está en los dieciséis bits centrales.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción localizable de la biblioteca.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directorio\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Directory](directory-table.md). Esta columna identifica la ruta de acceso de ayuda de la biblioteca de tipos. Esta columna se omite durante la publicidad.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Característica](feature-table.md). Esta columna especifica la característica que debe instalarse para que la biblioteca de tipos esté operativa.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo
</dt> <dd>

Costo asociado al registro de la biblioteca de tipos en bytes. Debe ser un número no negativo o null.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se hace referencia a esta tabla cuando se ejecuta [la acción RegisterTypeLibraries](registertypelibraries-action.md) o la acción [UnregisterTypeLibraries.](unregistertypelibraries-action.md)

El instalador escribe toda la información de registro de la biblioteca de tipos en la ubicación del Registro HKEY \_ LOCAL \_ MACHINE (HKLM). Este es el caso incluso para las instalaciones por usuario. Las bibliotecas de tipos no se pueden registrar en ubicaciones por usuario (HKCU).

Se recomienda encarecidamente a los autores de paquetes de instalación que no utilicen la tabla TypeLib. En su lugar, deben registrar bibliotecas de tipos mediante la [tabla Registry.](registry-table.md) Entre los motivos para evitar el registro propio se incluyen:

-   Si se produce un error en una instalación que usa la tabla TypeLib y se debe revertir, es posible que la reversión no restaure el equipo al mismo estado que existía antes de la reversión. Es posible que las bibliotecas de tipos registradas antes de la reversión no se registren después de la reversión.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



