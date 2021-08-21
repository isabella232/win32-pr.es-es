---
description: La tabla ReserveCost es una tabla opcional que permite al autor reservar una cantidad de espacio en disco en cualquier directorio que dependa del estado de instalación de un componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: ReserveCost Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df729e6afd66222bed3025991432354a7ec04023dcba17ce2bc5b5d81788827b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990408"
---
# <a name="reservecost-table"></a>ReserveCost Table

La tabla ReserveCost es una tabla opcional que permite al autor reservar una cantidad de espacio en disco en cualquier directorio que dependa del estado de instalación de un componente.

La tabla ReserveCost tiene las columnas siguientes.



| Columna        | Tipo                               | Clave | Nullable |
|---------------|------------------------------------|-----|----------|
| ReserveKey    | [Identificador](identifier.md)       | Y   | N        |
| Componente\_   | [Identificador](identifier.md)       | N   | N        |
| ReserveFolder | [Identificador](identifier.md)       | N   | Y        |
| ReserveLocal  | [DoubleInteger](doubleinteger.md) | N   | N        |
| ReserveSource | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey
</dt> <dd>

Clave principal que identifica de forma única una entrada de tabla ReserveCost.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa para la columna uno de la [tabla Component.](component-table.md) Reserva una cantidad de espacio especificada si se va a instalar este componente.

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder
</dt> <dd>

Esta columna contiene el nombre de una propiedad que es la ruta de acceso completa al directorio de destino. Este nombre de propiedad suele ser el nombre de un directorio de la tabla [Directory](directory-table.md) o el nombre de un conjunto de propiedades obtenido mediante la [acción Appsearch.](appsearch-action.md) Esto agrega la cantidad de espacio en disco especificado en ReserveLocal o ReserveSource al costo por volumen del dispositivo que contiene el directorio.

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal
</dt> <dd>

Número de bytes de espacio en disco que se reserva si el componente vinculado está instalado para ejecutarse localmente.

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource
</dt> <dd>

Número de bytes de espacio en disco que se reserva si el componente vinculado está instalado para ejecutarse desde el origen.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Reservar el costo de esta manera podría ser útil para los autores que quieran asegurarse de que una cantidad mínima de espacio en disco estará disponible una vez completada la instalación. Por ejemplo, este espacio en disco podría reservarse para documentos de usuario o para archivos de aplicación (como archivos de índice) que se crean solo después de iniciar la aplicación después de la instalación.

Puede usar la tabla ReserveCost para habilitar acciones personalizadas con el objeto de especificar un costo aproximado para los archivos, entradas del Registro u otros elementos que la acción personalizada pueda instalar. Las acciones personalizadas que agregan entradas a la tabla ReserveCost deben secuenciarse entre las acciones [CostInitialize](costinitialize-action.md) [y FileCost.](filecost-action.md) Esto es necesario para que la acción FileCost inicialice correctamente el costo de todos los componentes afectados por las entradas de la tabla ReserveCost.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



