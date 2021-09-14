---
description: Cómo selecciona Microsoft DVD Navigator la región de DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Cómo selecciona Microsoft DVD Navigator la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169913"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Cómo selecciona Microsoft DVD Navigator la región de DVD

El navegador de DVD de Microsoft usa el siguiente algoritmo para determinar la coincidencia de región mientras se reproducen discos DE DVD en un equipo:

1.  Dvd Navigator obtiene la región del disco, la región de unidad y la región del descodificador.
2.  Si la región del disco es "todas las regiones", el navegador de DVD reproduce el disco.
3.  Si el disco no está marcado para todas las regiones, el navegador de DVD comprueba si el descodificador tiene una región preestablecida.
4.  Si el descodificador tiene una región preestablecida y no coincide con la región del disco, el navegador de DVD devuelve un error que indica que no puede reproducir el disco en la configuración de DVD actual. (Salir)
5.  Si no se establece la región del descodificador o es la misma que la región del disco, el navegador de DVD comprueba si la región de unidad es la misma que la región del disco.
6.  Si la región de unidad coincide con la región del disco, el navegador de DVD reproduce el título.
7.  De lo contrario, si la región del controlador no coincide con la región del disco, el navegador de DVD invoca el código para cambiar la región de la unidad. Si se ha agotado el número permitido de cambios de región, se produce un error en el intento de cambio de región y el título no se puede reproducir en ese sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con el cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



