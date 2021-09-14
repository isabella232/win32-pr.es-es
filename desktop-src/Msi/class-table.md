---
description: La tabla Clase contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto. Cada fila puede generar un conjunto de claves y valores del Registro. La información de ProgId asociada se incluye en esta tabla.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabla de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158910"
---
# <a name="class-table"></a>Tabla de clases

La tabla Clase contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto. Cada fila puede generar un conjunto de claves y valores del Registro. La información de ProgId asociada se incluye en esta tabla.

La tabla Class tiene las siguientes columnas.



| Columna           | Tipo                         | Clave | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | Y   | N        |
| Context          | [Identificador](identifier.md) | Y   | N        |
| Componente\_      | [Identificador](identifier.md) | Y   | N        |
| ProgId \_ predeterminado  | [Texto](text.md)             | N   | Y        |
| Descripción      | [Texto](text.md)             | N   | Y        |
| Appid\_          | [GUID](guid.md)             | N   | Y        |
| FileTypeMask     | [Texto](text.md)             | N   | Y        |
| Icono\_           | [Identificador](identifier.md) | N   | Y        |
| IconIndex        | [Entero](integer.md)       | N   | Y        |
| DefInprocHandler | [Nombre de archivo](filename.md)     | N   | Y        |
| Argumento         | [Formato](formatted.md)   | N   | Y        |
| Característica\_        | [Identificador](identifier.md) | N   | N        |
| Atributos       | [Entero](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>Información de columna

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Identificador de clase (ID) de un servidor COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contexto
</dt> <dd>

Contexto del servidor para este servidor. Escriba uno de los siguientes valores para la clave CLSID.



| CLSID KEY                             | Descripción                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.             |
| [LocalServer32](../com/localserver32.md)   | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.             |
| [InprocServer](../com/inprocserver.md)     | Especifica la ruta de acceso a un archivo DLL del servidor en proceso.                           |
| [InprocServer32](../com/inprocserver32.md) | Especifica la ruta de acceso a un servidor en proceso de 32 bits y el modelo de subprocesos. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la [tabla Component](component-table.md) que especifica el componente cuyo archivo de clave proporciona el servidor COM.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ predeterminado
</dt> <dd>

Id. de programa predeterminado asociado a este identificador de clase. Esta columna es una clave externa en la [tabla ProgID](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción localizada asociada con el id. de clase y el identificador de programa.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>Appid\_
</dt> <dd>

Identificador de aplicación que contiene información de DCOM para la aplicación asociada [(GUID de cadena).](guid.md) Esta columna es una clave externa en la [tabla AppId](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contiene información para la clave HKCR (este CLSID).

Si existen varios patrones, deben delimitarse mediante un punto y coma y se generan subclaves numéricas: 0, 1, 2... Para obtener más información sobre esta funcionalidad, vea [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_
</dt> <dd>

Archivo que proporciona el icono asociado a este CLSID. El instalador escribe la entrada de esta columna en la clave DefaultIcon asociada al ProgId. Si no es NULL, la columna es una clave externa en la [tabla Icon](icon-table.md). Si es NULL, el servidor COM proporciona el recurso de icono. Las asociaciones de archivo y los accesos directos anunciados requieren un valor distinto de NULL en esta columna para mostrarse correctamente.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice de icono en el archivo de icono. Puede ser NULL.

Solo números no negativos.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Este campo especifica el controlador en proceso predeterminado para el contexto de servidor especificado en el campo Contexto.

Este campo debe ser Null si aparece una clave CLSID InprocServer o InprocServer en el campo Contexto.

Si aparece una clave CLSID LocalServer o LocalServer32 en el campo Contexto, el valor del campo DefInprocHandler identifica el controlador en proceso predeterminado.



| Value                | Descripción                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valor no numérico    | El instalador trata un valor no numérico en el campo DefInprocHandler como un archivo del sistema que sirve como controlador en proceso de 32 bits especificado por la clave InprocHandler32.                                                                                                            |
| Null                 | Los campos DefInprocHandler y Argument pueden ser NULL para una clave CLSID LocalServer o LocalServer32.                                                                                                                                                                           |
| 1 = valor predeterminado (sistema) | El valor predeterminado es el controlador en proceso de 16 bits especificado por InprocHandler. En este caso, el valor de InprocHandler es el nombre del Registro en el que se almacena el valor del controlador en proceso predeterminado. Por ejemplo, HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID.     |
| 2 = valor predeterminado (sistema) | El valor predeterminado es el controlador en proceso de 32 bits especificado por InprocHandler32. En este caso, el valor de InprocHandler32 es el nombre del Registro en el que se almacena el valor del controlador en proceso predeterminado. Por ejemplo, HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID. |
| 3 = valor predeterminado (sistema) | El valor predeterminado es un controlador en proceso de 16 o 32 bits.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Si aparece una clave CLSID LocalServer o LocalServer32 en el campo Contexto, el texto de este campo se registra como argumento en el servidor y COM lo usa para invocar el servidor. Los campos DefInprocHandler y Argument pueden ser NULL si LocalServer o LocalServer32 aparecen en el campo Contexto.

Tenga en cuenta que la resolución de propiedades en el campo Argumento es limitada. Una propiedad con formato Propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando se instala el componente propietario \[ \] de la clase. Por ejemplo, para que el argumento "MyDoc.doc" se resuelva en el valor correcto, el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee \[ \# la clase \] .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa en la [tabla Característica](feature-table.md) que especifica la característica que proporciona el servidor COM.

Clave externa para la columna uno de la tabla Característica.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Si **msidbClassAttributesRelativePath** se establece en esta columna, se puede usar el nombre de archivo sin sistema para los servidores COM. El instalador solo registra el nombre de archivo en lugar de la ruta de acceso completa. Esto permite que el servidor del directorio actual tome prioridad y permite varias copias del mismo componente.



| Atributo                            | Decimal | Hexadecimal |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta [la acción RegisterClassInfo](registerclassinfo-action.md) o [la acción UnregisterClassInfo.](unregisterclassinfo-action.md)

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

 

 
