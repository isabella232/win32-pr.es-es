---
description: Cómo selecciona el navegador de DVD de Microsoft la región de DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Cómo selecciona el navegador de DVD de Microsoft la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677041"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Cómo selecciona el navegador de DVD de Microsoft la región de DVD

El navegador de DVD de Microsoft usa el siguiente algoritmo para determinar la coincidencia de región mientras se reproducen discos DVD en un equipo:

1.  El navegador de DVD obtiene la región del disco, la región de la unidad y la región del descodificador.
2.  Si la región de disco es "todas las regiones", el navegador de DVD reproduce el disco.
3.  Si el disco no está marcado para todas las regiones, el explorador de DVD comprueba si el descodificador tiene una región preestablecida.
4.  Si el descodificador tiene una región preestablecida y no coincide con la región de disco, el navegador de DVD devuelve un error que indica que no puede reproducir el disco en la configuración actual del DVD. Abandonar
5.  Si la región del descodificador no está establecida o es la misma que la región del disco, el explorador de DVD comprueba si la región de la unidad es la misma que la región de disco.
6.  Si la región de unidad coincide con la región de disco, el explorador de DVD reproduce el título.
7.  De lo contrario, si la región del controlador no coincide con la región del disco, el navegador de DVD invoca el código para cambiar la región de la unidad. Si se ha agotado el número permitido de cambios en la región, se produce un error en el intento de cambio de región y no se puede reproducir el título en ese sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad de cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



