---
description: Las estructuras de datos que usa TSPI son idénticas a las definidas en estructuras TAPI, con la excepción de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Estructuras TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687484"
---
# <a name="tspi-structures"></a>Estructuras TSPI

Las estructuras de datos que usa TSPI son idénticas a las definidas en [estructuras TAPI](./tapi-structures.md), con la excepción de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

En el caso de la mayoría de las estructuras de datos más grandes, la responsabilidad de rellenar los miembros se divide entre el proveedor de servicios y TAPI. El proveedor de servicios debe conservar los valores presentes en los miembros que pertenecen a TAPI. La descripción de los miembros que debe establecer el proveedor de servicios y que debe conservarse se proporciona en la sección funciones de las funciones que hacen referencia a esa estructura de datos.

Para cada estructura, en la sección de referencia se enumeran los elementos siguientes:

-   El propósito de la estructura
-   Una descripción de los valores o campos
-   Descripción de la extensibilidad de la estructura.
-   Comentarios opcionales sobre el uso de la estructura
-   Referencias opcionales a otras funciones, mensajes, constantes o estructuras.

La memoria de todas las estructuras de datos cuya representación se publica y comparte con TAPI y el proveedor de servicios se asigna mediante TAPI o una aplicación que utiliza TAPI. TAPI pasa un puntero a la función TSPI que devuelve la información. TSPI rellena la estructura de datos con la información solicitada. Si la operación es asincrónica, la información no estará disponible hasta que la devolución de llamada de respuesta asincrónica indique Success.

> [!Note]  
> Algunas estructuras incluyen campos de tamaño y desplazamiento para definir la ubicación y la longitud de las cadenas en la parte variable de la estructura. Si se solicita al proveedor de servicios que agregue una cadena pero no hay ninguna cadena disponible, el proveedor de servicios debe indicar esta condición de una de estas maneras:
>
> -   Establezca los campos tamaño y desplazamiento en 0.
> -   Establezca el campo desplazamiento en distinto de cero, pero el tamaño en 0.
> -   Establezca el campo desplazamiento en distinto de cero, el tamaño en 1 y el byte en el desplazamiento en 0.

 

 

 
