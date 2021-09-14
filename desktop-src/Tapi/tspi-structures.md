---
description: Las estructuras de datos que usa TSPI son idénticas a las definidas en estructuras TAPI, a excepción de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Estructuras TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173073"
---
# <a name="tspi-structures"></a>Estructuras TSPI

Las estructuras de datos que usa TSPI son idénticas a las definidas en [estructuras TAPI,](./tapi-structures.md)a excepción de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

En el caso de la mayoría de las estructuras de datos más grandes, la responsabilidad de rellenar miembros se divide entre el proveedor de servicios y TAPI. El proveedor de servicios debe conservar los valores presentes en los miembros que pertenecen a TAPI. La descripción de qué miembros debe establecer el proveedor de servicios y cuáles deben conservarse se proporciona en la sección Funciones de las funciones que hacen referencia a esa estructura de datos.

Para cada estructura, la sección de referencia enumera los siguientes elementos:

-   El propósito de la estructura
-   Descripción de los valores o campos
-   Descripción de la extensibilidad de la estructura
-   Comentarios opcionales sobre el uso de la estructura
-   Referencias opcionales a otras funciones, mensajes, constantes o estructuras.

TapI o una aplicación que usa TAPI asignan memoria para todas las estructuras de datos cuya representación se publica y comparte tanto tapi como el proveedor de servicios. TAPI pasa un puntero a la función TSPI que devuelve la información. TSPI rellena la estructura de datos con la información solicitada. Si la operación es asincrónica, la información no está disponible hasta que la devolución de llamada de respuesta asincrónica indica que se ha completado correctamente.

> [!Note]  
> Algunas estructuras incluyen los campos Tamaño y Desplazamiento para definir la ubicación y la longitud de las cadenas en la parte variable de la estructura. Si se solicita al proveedor de servicios que agregue una cadena pero no hay ninguna cadena disponible, el proveedor de servicios debe indicar esta condición de una de estas maneras:
>
> -   Establezca los campos Tamaño y Desplazamiento en 0.
> -   Establezca el campo Desplazamiento en distinto de cero pero Tamaño en 0.
> -   Establezca el campo Offset en distinto de cero, Size en 1 y el byte en Offset en 0.

 

 

 
