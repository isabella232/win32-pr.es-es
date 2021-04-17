---
description: Este atributo mide hasta qué punto se rellena la barra del indicador de progreso.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Atributo de control de progreso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653037"
---
# <a name="progress-control-attribute"></a>Atributo de control de progreso

Este atributo mide hasta qué punto se rellena la barra del indicador de progreso. El registro contiene dos enteros y una cadena. El primer número es el progreso, el segundo número es el intervalo (el número máximo posible para el progreso). Al establecer, los enteros se pueden especificar como campos de tipo entero o cadenas que contengan los enteros. Si falta el segundo número, se supone que es el valor predeterminado (1024). Si el progreso es mayor que el intervalo, se cambia para que sea el intervalo. El tercer campo es una cadena, el nombre de la acción cuyo progreso se muestra.

Para obtener información relacionada, vea [crear un control ProgressBar](authoring-a-progressbar-control.md)y [Agregar acciones personalizadas a ProgressBar](adding-custom-actions-to-the-progressbar.md).

## <a name="valid-controls"></a>Controles válidos

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Marcas de bits asociadas

Este atributo no utiliza marcas de bits.

## <a name="remarks"></a>Observaciones

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



