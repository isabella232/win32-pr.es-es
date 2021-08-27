---
description: Este atributo mide hasta qué punto se llena la barra del indicador de progreso.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Atributo de control progress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a867772ff1452087ab22da76d3c1f93aea32e5ad50bd23ffe8ace62889086781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074635"
---
# <a name="progress-control-attribute"></a>Atributo de control progress

Este atributo mide hasta qué punto se llena la barra del indicador de progreso. El registro contiene dos enteros y una cadena. El primer número es el progreso, el segundo es el intervalo (el número máximo posible para el progreso). En el valor , los enteros se pueden especificar como campos enteros o cadenas que contienen los enteros. Si falta el segundo número, se supone que es el valor predeterminado (1024). Si el progreso es mayor que el intervalo, se cambia para que sea el intervalo. El tercer campo es una cadena, el nombre de la acción cuyo progreso se muestra.

Para obtener información relacionada, [vea Crear un control ProgressBar y](authoring-a-progressbar-control.md)Agregar acciones [personalizadas a ProgressBar](adding-custom-actions-to-the-progressbar.md).

## <a name="valid-controls"></a>Controles válidos

[Progressbar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Marcas de bits asociadas

Este atributo no usa marcas de bits.

## <a name="remarks"></a>Comentarios

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



