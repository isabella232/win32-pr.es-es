---
description: La tabla de entorno se utiliza para establecer los valores de las variables de entorno.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Tabla de entorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a4db2e33c01685bdc40475f659e1b03b69b6c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687326"
---
# <a name="environment-table"></a>Tabla de entorno

La tabla de entorno se utiliza para establecer los valores de las variables de entorno.

La tabla de entorno tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Entorno | [Identificador](identifier.md) | Y   | N        |
| Nombre        | [Texto](text.md)             | N   | N        |
| Value       | [Formatea](formatted.md)   | N   | Y        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Entorno
</dt> <dd>

Esta es la clave principal de la tabla y es un token no localizado.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Esta columna es el nombre traducible de la variable de entorno. Los valores de clave se escriben o se quitan en función de cuál de los caracteres de la tabla siguiente se antepone al nombre. No hay ningún efecto en el orden de los símbolos que se usan en un prefijo.



| Prefijo                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Cree la variable de entorno si no existe y, a continuación, establézcala durante la instalación. Si existe la variable de entorno, establézcala durante la instalación.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Cree la variable de entorno si no existe y, a continuación, establézcala durante la instalación. Esto no tiene ningún efecto en el valor de la variable de entorno si ya existe.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Quite la variable de entorno cuando se quite el componente. Este símbolo se puede combinar con cualquier prefijo.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Quite la variable de entorno durante una instalación. El instalador solo quita una variable de entorno durante una instalación si el nombre y el valor de la variable coinciden con las entradas de los campos de nombre y valor de la tabla de entorno. Si desea quitar una variable de entorno, independientemente de su valor, use la sintaxis '! ' y deje vacío el campo de valor.                                                                                                                    |
| \*                             | Este prefijo se usa con Windows 2000 para indicar que el nombre hace referencia a una variable de entorno del sistema. Si no hay ningún asterisco, el instalador escribe la variable en el entorno del usuario. Este símbolo se puede combinar con cualquier prefijo. Un paquete que se usa para la instalación en el contexto de [instalación](installation-context.md) por equipo debe escribir variables de entorno en el entorno del equipo incluyendo \* en la columna nombre. Para obtener más información, vea la sección Comentarios. |
| =-                             | La variable de entorno se establece en Install (instalar) y se quita durante la desinstalación. Este es el comportamiento habitual.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Quita una variable de entorno durante una instalación o desinstalación.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Estos no son prefijos válidos                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Si el campo de valor de la tabla incluye \[ ~ \] , los caracteres de prefijo solo se aplican a la parte especificada de la cadena. El uso de \[ ~ \] se describe a continuación en la sección de la columna valor.

La variable de entorno se quita si el campo de valor de la tabla está en blanco. Por lo tanto, con un espacio en blanco en el campo de valor, el prefijo = elimina la variable de entorno al instalar y el prefijo--elimina los valores actuales al desinstalar.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta columna contiene el valor traducible que se va a establecer como una cadena con formato. Vea [con formato](formatted.md). Si este campo se deja en blanco, se quita la variable. Si el campo está en blanco y la cadena del campo nombre está precedida por el símbolo-, la variable solo se quita cuando se quita el componente.

Para anexar un valor al final de una variable existente, anteponga a la cadena de este campo el carácter nulo \[ ~ \] y el carácter separador. Por ejemplo, si el punto y coma es el separador elegido: \[ ~ \] ;*Valor*.

Para anteponer un valor a la parte delantera de una variable existente, anexe la cadena de este campo por el carácter separador y el carácter nulo \[ ~ \] . Por ejemplo, si el punto y coma es el separador elegido: *valor*; \[ ~ \] .

Si no \[ ~ \] existe en el campo, la cadena representa el valor completo que se va a establecer o eliminar.

Cada fila solo puede contener un valor. Por ejemplo, el *valor* de entrada; *Valor* \[ ~ ; \] es más de un valor y no debe usarse porque produce resultados imprevisibles. *Valor* de entrada; \[ ~ \] es solo un valor.

Si el nombre tiene el prefijo +, \[ ~ \] no se debe usar en la columna valor. Esto se debe a que el significado de "+" y " \[ ~ \] " son claramente excluyentes entre sí.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Una clave externa a la primera columna de la [tabla de componentes](component-table.md). Esta columna hace referencia al componente que controla la instalación de los valores de entorno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para que el instalador establezca las variables de entorno, la acción [WriteEnvironmentStrings](writeenvironmentstrings-action.md) y la [acción RemoveEnvironmentStrings](removeenvironmentstrings-action.md) deben aparecer en la [tabla InstallExecuteSequence](installexecutesequence-table.md).

Tenga en cuenta que las variables de entorno no cambian para la instalación en curso cuando se ejecutan las acciones [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) . En Windows 2000, esta información se almacena en el registro y un mensaje notifica al sistema los cambios cuando se completa la instalación. Un nuevo proceso u otro proceso que comprueba estos mensajes utiliza las nuevas variables de entorno.

Cuando modifique la variable de entorno PATH con la tabla de entorno, no intente escribir la ruta de acceso completa explícitamente en el campo de valor. En su lugar, extienda la ruta de acceso existente prefijando o anexando un valor y un delimitador (;) a \[ ~ \] . Si \[ ~ \] no está presente en el campo de valor, se pierde la información de la ruta de acceso existente y la instalación del archivo. msi puede impedir el arranque del equipo. Normalmente, la variable de ruta de acceso se establece mediante la sintaxis: \[ ~ \] ; Valor.

Al realizar instalaciones por equipo desde un servidor de Terminal Server, el instalador escribe variables de entorno por usuario en **HKU \\ . \\Entorno predeterminado**. Dado que Terminal Services no Replica esta sección del registro, la instalación no establece las variables de entorno por usuario. Un paquete que se usa para las instalaciones por máquina debe escribir variables de entorno en el entorno del equipo mediante \* la inclusión de en la columna nombre. Si el paquete se puede instalar por usuario o por equipo, cree dos componentes: (1) un componente por usuario con las entradas de la tabla de entorno creadas para la configuración de usuario, y (2) un componente por equipo con la tabla de entorno creada para la configuración del equipo. Condición de la instalación de este componente mediante la propiedad [**privileged**](privileged.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE65](ice65.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
</dl>

 

 




