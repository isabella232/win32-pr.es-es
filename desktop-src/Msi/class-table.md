---
description: La tabla de clases contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto. Cada fila puede generar un conjunto de claves y valores del registro. La información asociada de ProgId se incluye en esta tabla.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabla de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666995"
---
# <a name="class-table"></a>Tabla de clases

La tabla de clases contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto. Cada fila puede generar un conjunto de claves y valores del registro. La información asociada de ProgId se incluye en esta tabla.

La tabla de la clase tiene las columnas siguientes.



| Columna           | Tipo                         | Clave | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | Y   | N        |
| Context          | [Identificador](identifier.md) | Y   | N        |
| Componente\_      | [Identificador](identifier.md) | Y   | N        |
| \_Valor predeterminado de ProgID  | [Texto](text.md)             | N   | Y        |
| Descripción      | [Texto](text.md)             | N   | Y        |
| AppId\_          | [GUID](guid.md)             | N   | Y        |
| FileTypeMask     | [Texto](text.md)             | N   | Y        |
| Icono\_           | [Identificador](identifier.md) | N   | Y        |
| IconIndex        | [Entero](integer.md)       | N   | Y        |
| DefInprocHandler | [Nombre de archivo](filename.md)     | N   | Y        |
| Argumento         | [Formatea](formatted.md)   | N   | Y        |
| Característica\_        | [Identificador](identifier.md) | N   | N        |
| Atributos       | [Entero](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>Información de columna

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Identificador de clase (ID.) de un servidor COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contexto
</dt> <dd>

El contexto de servidor para este servidor. Escriba uno de los siguientes valores para la clave CLSID.



| CLAVE CLSID                             | Descripción                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.             |
| [LocalServer32](../com/localserver32.md)   | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.             |
| [InprocServer](../com/inprocserver.md)     | Especifica la ruta de acceso a un archivo DLL de servidor en proceso.                           |
| [InprocServer32](../com/inprocserver32.md) | Especifica la ruta de acceso a un servidor de proceso de 32 bits y al modelo de subprocesos. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la [tabla de componentes](component-table.md) que especifica el componente cuyo archivo de clave proporciona el servidor com.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>\_Valor predeterminado de ProgID
</dt> <dd>

IDENTIFICADOR de programa predeterminado asociado a este identificador de clase. Esta columna es una clave externa de la [tabla ProgID](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Descripción localizada asociada con el identificador de clase y el ID. de programa.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_
</dt> <dd>

IDENTIFICADOR de la aplicación que contiene información de DCOM para la aplicación asociada ( [GUID](guid.md)de cadena). Esta columna es una clave externa en la [tabla AppID](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contiene información de la clave HKCR (este CLSID).

Si existen varios patrones, deben delimitarse con un punto y coma, y se generan subclaves numéricas: 0, 1, 2... Para obtener más información acerca de esta funcionalidad, vea [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_
</dt> <dd>

Archivo que proporciona el icono asociado a este CLSID. El instalador escribe la entrada en esta columna en la clave DefaultIcon asociada al ProgId. Si no es null, la columna es una clave externa en la [tabla de iconos](icon-table.md). Si es null, el servidor COM proporciona el recurso de icono. Los accesos directos y las asociaciones de archivos anunciados requieren un valor distinto de NULL en esta columna para que se muestren correctamente.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice del icono en el archivo de icono. Puede ser NULL.

Solo números no negativos.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Este campo especifica el controlador de in-Process predeterminado para el contexto de servidor especificado en el campo de contexto.

Este campo debe ser null si aparece una clave CLSID de InprocServer o InprocServer en el campo de contexto.

Si aparece una clave CLSID de LocalServer o LocalServer32 en el campo de contexto, el valor del campo DefInprocHandler identifica el controlador en proceso predeterminado.



| Value                | Descripción                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valor no numérico    | El instalador trata un valor no numérico en el campo DefInprocHandler como un archivo del sistema que actúa como el controlador en proceso de 32 bits especificado por la clave InprocHandler32.                                                                                                            |
| Null                 | Los campos DefInprocHandler y argument pueden ser null para una clave CLSID LocalServer o LocalServer32.                                                                                                                                                                           |
| 1 = valor predeterminado (sistema) | El valor predeterminado es el controlador en proceso de 16 bits especificado por InprocHandler. En este caso, el valor de InprocHandler es el nombre del registro en el que se almacena el valor del controlador en proceso predeterminado. Por ejemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID.     |
| 2 = valor predeterminado (sistema) | El valor predeterminado es el controlador en proceso de 32 bits especificado por InprocHandler32. En este caso, el valor de InprocHandler32 es el nombre del registro en el que se almacena el valor del controlador en proceso predeterminado. Por ejemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID. |
| 3 = valor predeterminado (sistema) | El valor predeterminado es un controlador en proceso de 16 ó 32 bits.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Si aparece una clave CLSID de LocalServer o LocalServer32 en el campo de contexto, el texto de este campo se registra como argumento en el servidor y COM lo usa para invocar el servidor. Los campos DefInprocHandler y argument pueden ser null si se muestra LocalServer o LocalServer32 en el campo de contexto.

Tenga en cuenta que la resolución de propiedades en el campo argumento es limitada. Una propiedad con formato \[ \] de propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando el componente propietario de la clase está instalado. Por ejemplo, para que el argumento " \[ \#MyDoc.doc\] " resuelva el valor correcto, el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee la clase.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_
</dt> <dd>

Clave externa en la [tabla de características](feature-table.md) que especifica la característica que proporciona el servidor com.

Clave externa para la columna uno de la tabla de características.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Si **msidbClassAttributesRelativePath** se establece en esta columna, el nombre de archivo no operativo se puede usar para servidores com. El instalador solo registra el nombre de archivo en lugar de la ruta de acceso completa. Esto permite que el servidor del directorio actual tenga prioridad y permita varias copias del mismo componente.



| Atributo                            | Decimal | Hexadecimal |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterClassInfo](registerclassinfo-action.md) o la [acción UnregisterClassInfo](unregisterclassinfo-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
