---
description: La tabla ReserveCost es una tabla opcional que permite al autor reservar una cantidad de espacio en disco en cualquier directorio que dependa del estado de instalación de un componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Tabla ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002196"
---
# <a name="reservecost-table"></a>Tabla ReserveCost

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

Clave principal que identifica de forma única una entrada de la tabla ReserveCost.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa para la columna uno de la tabla de [componentes](component-table.md) . Reserva una cantidad especificada de espacio si se va a instalar este componente.

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder
</dt> <dd>

Esta columna contiene el nombre de una propiedad que es la ruta de acceso completa al directorio de destino. Este nombre de propiedad suele ser el nombre de un directorio en la tabla del [directorio](directory-table.md) o el nombre de un conjunto de propiedades obtenido mediante la acción [AppSearch](appsearch-action.md) . Esto agrega la cantidad de espacio en disco especificada en ReserveLocal o ReserveSource al costo del volumen del dispositivo que contiene el directorio.

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal
</dt> <dd>

El número de bytes de espacio en disco que se reservan si el componente vinculado está instalado para ejecutarse localmente.

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource
</dt> <dd>

El número de bytes de espacio en disco que se reservan si el componente vinculado está instalado para ejecutarse desde el origen.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El costo de la reserva de esta manera podría ser útil para los autores que deseen asegurarse de que habrá una cantidad mínima de espacio en disco disponible una vez completada la instalación. Por ejemplo, puede que este espacio en disco esté reservado para documentos de usuario o para archivos de aplicación (como archivos de índice) que se crean solo después de que la aplicación se inicie después de la instalación.

Puede usar la tabla ReserveCost para habilitar las acciones personalizadas con el fin de especificar un costo aproximado para los archivos, entradas del registro u otros elementos que pueda instalar la acción personalizada. Las acciones personalizadas que agregan entradas a la tabla ReserveCost se deben secuenciar entre las acciones [CostInitialize](costinitialize-action.md) y [FileCost](filecost-action.md) . Esto es necesario para que la acción FileCost inicialice correctamente el costo de todos los componentes afectados por las entradas de la tabla ReserveCost.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



