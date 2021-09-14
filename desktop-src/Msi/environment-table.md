---
description: La tabla Entorno se usa para establecer los valores de las variables de entorno.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Tabla de entorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a4db2e33c01685bdc40475f659e1b03b69b6c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158476"
---
# <a name="environment-table"></a>Tabla de entorno

La tabla Entorno se usa para establecer los valores de las variables de entorno.

La tabla Environment tiene las siguientes columnas.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Entorno | [Identificador](identifier.md) | Y   | N        |
| Nombre        | [Texto](text.md)             | N   | N        |
| Value       | [Formato](formatted.md)   | N   | Y        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Ambiente
</dt> <dd>

Esta es la clave principal de la tabla y es un token no localizado.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Esta columna es el nombre localizable de la variable de entorno. Los valores de clave se escriben o quitan en función de cuál de los caracteres de la tabla siguiente tiene como prefijo el nombre. No hay ningún efecto en el orden de los símbolos usados en un prefijo.



| Prefijo                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Cree la variable de entorno si no existe y, a continuación, esta establezca durante la instalación. Si la variable de entorno existe, esta establezca durante la instalación.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Cree la variable de entorno si no existe y, a continuación, esta establezca durante la instalación. Esto no tiene ningún efecto en el valor de la variable de entorno si ya existe.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Quite la variable de entorno cuando se quite el componente. Este símbolo se puede combinar con cualquier prefijo.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Quite la variable de entorno durante una instalación. El instalador solo quita una variable de entorno durante una instalación si el nombre y el valor de la variable coinciden con las entradas de los campos Nombre y Valor de la tabla Entorno. Si desea quitar una variable de entorno, independientemente de su valor, use la sintaxis '!' y deje el campo Valor vacío.                                                                                                                    |
| \*                             | Este prefijo se usa con Windows 2000 para indicar que el nombre hace referencia a una variable de entorno del sistema. Si no hay ningún asterisco, el instalador escribe la variable en el entorno del usuario. Este símbolo se puede combinar con cualquier prefijo. Un paquete que se usa para [](installation-context.md) la instalación en el contexto de instalación por equipo debe escribir variables de entorno en el entorno de la máquina incluyendo en \* la columna Nombre . Para obtener más información, vea la sección Comentarios. |
| =-                             | La variable de entorno se establece al instalar y se quita al desinstalar. Este es el comportamiento habitual.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Quita una variable de entorno durante una instalación o desinstalación.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Estos no son prefijos válidos                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Si el campo Valor de la tabla incluye , los caracteres de prefijo solo se aplican a \[ ~ \] la parte especificada de la cadena. El uso de \[ ~ \] se describe a continuación en la sección Columna valor .

La variable de entorno se quita si el campo Valor de la tabla está en blanco. Por lo tanto, con un valor en blanco en el campo Valor, un prefijo = elimina la variable de entorno al instalar y un prefijo - elimina los valores actuales en la desinstalación.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta columna contiene el valor localizable que se va a establecer como una cadena con formato. Vea [Formatted](formatted.md). Si este campo se deja en blanco, se quita la variable. Si el campo está en blanco y la cadena del campo Nombre tiene como prefijo el símbolo - , la variable solo se quita cuando se quita el componente.

Para anexar un valor al final de una variable existente, antefijo la cadena de este campo por el carácter null \[ ~ \] y el carácter separador. Por ejemplo, si el punto y coma es el separador elegido: \[ ~ \] ;*Valor*.

Para antefijo de un valor al frente de una variable existente, anexe la cadena de este campo por el carácter separador y el carácter nulo \[ ~ \] . Por ejemplo, si el punto y coma es el separador elegido: *Valor*; \[ ~ \] .

Si no \[ ~ \] hay ningún en el campo, la cadena representa el valor completo que se va a establecer o eliminar.

Cada fila solo puede contener un valor. Por ejemplo, la entrada *Value*; *Value*; \[ ~ \] es más de un valor y no se debe usar porque produce resultados impredecibles. La entrada *Value*; \[ ~ \] es solo un valor.

Si Name tiene el prefijo +, \[ ~ \] no se debe usar en la columna Valor. Esto se debe a que el significado de "+" y " \[ ~ \] " es claramente excluyente entre sí.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa de la primera columna de la [tabla Component](component-table.md). Esta columna hace referencia al componente que controla la instalación de los valores de entorno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para que el instalador establezca variables de entorno, la acción [WriteEnvironmentStrings](writeenvironmentstrings-action.md) y la acción [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) deben aparecer en la tabla [InstallExecuteSequence](installexecutesequence-table.md).

Tenga en cuenta que las variables de entorno no cambian para la instalación en curso cuando se ejecutan la acción [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o [RemoveEnvironmentStrings.](removeenvironmentstrings-action.md) En Windows 2000, esta información se almacena en el Registro y un mensaje notifica al sistema los cambios cuando se completa la instalación. Un nuevo proceso u otro proceso que comprueba estos mensajes usa las nuevas variables de entorno.

Al modificar la variable de entorno path con la tabla Environment, no intente especificar explícitamente la nueva ruta de acceso completa en el campo Valor. En su lugar, extienda la ruta de acceso existente mediante el prefijo o la anexación de un valor y un delimitador (;) a \[ ~ \] . Si no está presente en el campo Valor, la información de ruta de acceso existente se pierde y la instalación del archivo .msi puede impedir que el equipo \[ ~ \] arranque. La variable de ruta de acceso se establece normalmente mediante la sintaxis : \[ ~ \] ; Valor.

Al realizar instalaciones por máquina desde un servidor de terminal Server, el instalador escribe variables de entorno por usuario en **\\ HKU. Entorno \\ predeterminado.** Dado que Terminal Services no replica esta sección del Registro, la instalación no establece las variables de entorno por usuario. Un paquete usado para las instalaciones por equipo debe escribir variables de entorno en el entorno del equipo incluyendo \* en la columna Nombre . Si el paquete se puede instalar por usuario o por equipo, cree dos componentes: (1) un componente por usuario con las entradas de la tabla Entorno creadas para la configuración de usuario y (2) un componente por equipo con la tabla Entorno creada para la configuración del equipo. Condición de la instalación de este componente mediante la [**propiedad Privileged.**](privileged.md)

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

 

 




