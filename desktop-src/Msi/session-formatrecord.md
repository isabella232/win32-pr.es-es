---
description: El método FormatRecord del objeto Session devuelve una cadena con formato a partir de una plantilla y registra datos.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Método Session.FormatRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f58aabc0bd222b22ee74cb0b431ce8051ed6bad546d963160c922bd86dee2383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629155"
---
# <a name="sessionformatrecord-method"></a>Método Session.FormatRecord

El **método FormatRecord** del [**objeto Session**](session-object.md) devuelve una cadena con formato a partir de una plantilla y registra datos.

## <a name="syntax"></a>Sintaxis


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*record* 
</dt> <dd>

Objeto **Record** requerido que contiene una plantilla y datos a los que se va a dar formato. La cadena de plantilla debe establecerse en el campo 0 seguido de los parámetros de datos a los que se hace referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **método FormatRecord** usa el siguiente proceso de formato.

Los parámetros [a los que se](formatted.md) va a dar formato se incluyen entre corchetes . \[ \] . Los corchetes se pueden iterar porque las sustituciones se resuelven desde dentro hacia fuera.

Si una parte de la cadena se incluye entre llaves { } y no contiene corchetes, la parte se deja sin modificar, incluidas las llaves.

Si una parte de la cadena está entre llaves y contiene uno o varios nombres de propiedad, y si se encuentran todas las propiedades, el texto (con las sustituciones resueltas) se muestra sin llaves. Si no se encuentra ninguna de las propiedades, se quita todo el texto de las llaves y las propias llaves.

**Para dar formato a cadenas mediante el método FormatRecord**

1.  Los parámetros numéricos se sustituyen reemplazando el marcador por el valor del campo de registro correspondiente, con valores nulos o ausentes que no producen texto.
2.  La cadena que da como resultado se procesa reemplazando los parámetros que no son de registro por los valores correspondientes, como se indica en las descripciones siguientes.
    -   Si se encuentra una subcadena con el formato " \[ propertyname ", se reemplaza por el valor de la propiedad \] .
    -   Si se encuentra una subcadena con el formato \[ "%environmentvariable", se sustituye el valor de \] la variable de entorno.
    -   Si se encuentra una subcadena de la clave de archivo de formulario, se reemplaza por la ruta de acceso completa del archivo, por la clave de archivo de valor usada como clave en la \[ \#  \] [tabla File](file-table.md).  El valor de filekey permanece en blanco y no se reemplaza por una ruta de acceso hasta que el instalador ejecuta la acción \[ \#  \] [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y [la acción CostFinalize](costfinalize-action.md). El valor de \[ \# *filekey* \] depende del estado de instalación del componente al que pertenece el archivo. Si el componente se ejecuta desde el origen, el valor es la ruta de acceso a la ubicación de origen del archivo. Si el componente se ejecuta localmente, el valor es la ruta de acceso a la ubicación de destino del archivo después de la instalación. Si el componente está ausente, la ruta de acceso está en blanco. Para obtener más información sobre cómo comprobar el estado de instalación de los componentes, vea Comprobar la [instalación de características, componentes, archivos](checking-the-installation-of-features-components-files.md).
    -   Si se encuentra una subcadena con el formato $componentkey, se reemplaza por el directorio de instalación del componente, por el valor \[  \] *componentkey* usado como clave en la tabla [Component](component-table.md). El valor de componentkey permanece en blanco y no se reemplaza por un directorio hasta que el instalador ejecuta la acción \[ $  \] [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y [la acción CostFinalize](costfinalize-action.md). El valor de \[ $ *componentkey* \] depende del estado de instalación del componente. Si el componente se ejecuta desde el origen, el valor es el directorio de origen del archivo. Si el componente se ejecuta localmente, el valor es el directorio de destino después de la instalación. Si el componente está ausente, el valor se deja en blanco. Para obtener más información sobre cómo comprobar el estado de instalación de los componentes, vea Comprobar la [instalación de características, componentes, archivos](checking-the-installation-of-features-components-files.md).
    -   Si se encuentra una subcadena con el formato " c ", se reemplaza por \[ \\ el carácter sin ningún \] procesamiento adicional. Solo se conserva el primer carácter después de la barra diagonal inversa; se quita todo lo demás.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Formato](formatted.md)
</dt> <dt>

[Tipos de datos de columna](column-data-types.md)
</dt> </dl>

 

 




