---
description: Este atributo mide hasta qué punto se rellena la barra del indicador de progreso.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Atributo de control de progreso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074325"
---
# <a name="progress-control-attribute"></a>Atributo de control de progreso

Este atributo mide hasta qué punto se rellena la barra del indicador de progreso. El registro contiene dos enteros y una cadena. El primer número es el progreso, el segundo es el intervalo (el número máximo posible para el progreso). Al establecer, los enteros se pueden especificar como campos enteros o cadenas que contienen los enteros. Si falta el segundo número, se supone que es el valor predeterminado (1024). Si el progreso es mayor que el intervalo, se cambia para que sea el intervalo. El tercer campo es una cadena, el nombre de la acción cuyo progreso se muestra.

Para obtener información relacionada, [vea Crear un control ProgressBar y](authoring-a-progressbar-control.md)Agregar acciones [personalizadas a ProgressBar.](adding-custom-actions-to-the-progressbar.md)

## <a name="valid-controls"></a>Controles válidos

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Marcas de bits asociadas

Este atributo no usa marcas de bits.

## <a name="remarks"></a>Observaciones

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



