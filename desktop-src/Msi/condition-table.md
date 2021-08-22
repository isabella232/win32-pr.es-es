---
description: La tabla Condition se puede usar para modificar el estado de selección de cualquier entrada de la tabla Feature basada en una expresión condicional.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabla de condiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d9ccb265d69f99a58e155657a0e9d058ba61a920088184ec2b67c3e4506a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926965"
---
# <a name="condition-table"></a>Tabla de condiciones

La tabla Condition se puede usar para modificar el estado de selección de cualquier entrada de la [tabla Feature](feature-table.md) basada en una expresión condicional.

La tabla Condition tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Característica\_ | [Identificador](identifier.md) | Y   | N        |
| Nivel     | [Entero](integer.md)       | Y   | N        |
| Condición | [Condition](condition.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa en la columna uno de la tabla Característica.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Nivel
</dt> <dd>

Nivel de instalación condicional para la característica en la columna \_ Característica de esta tabla. El instalador establece el nivel de instalación de esta característica en el nivel especificado en esta columna si la expresión de la columna Condición se evalúa como TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Si esta expresión condicional se evalúa como TRUE, la columna Level de la tabla Feature se establece en el nivel de instalación condicional.

La expresión de la columna Condición no debe contener referencia al estado instalado de ninguna característica o componente. Esto se debe a que las expresiones de la columna Condición se evalúan antes de que el instalador evalúe los estados instalados de características y componentes. Cualquier expresión de la tabla Condición que intente comprobar el estado instalado de una característica o componente siempre se evalúa como false.

Para obtener información sobre la sintaxis de las instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una característica se puede deshabilitar permanentemente estableciendo la columna Nivel en 0.

El nivel se puede establecer en función de cualquier instrucción condicional, como una prueba de la plataforma, el sistema operativo o una configuración de propiedad determinada.

Las condiciones deben elegirse cuidadosamente para que una característica no esté habilitada en la instalación y, a continuación, se deshabilite en la desinstalación. Esto huérfanará la característica y el producto no se podrá desinstalar.

Se hace referencia a esta tabla cuando se ejecuta la [acción CostFinalize.](costfinalize-action.md)

Si la [**propiedad Preselected**](preselected.md) se ha establecido en 1, el instalador no evalúa la tabla Condition. La tabla Condición solo afecta a la instalación de características cuando no se ha establecido ninguna de las siguientes propiedades:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**eliminar**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**Reinstalar**](reinstall.md)  
[**Anunciar**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



