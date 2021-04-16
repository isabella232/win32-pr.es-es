---
description: Cambio posterior de la región de DVD
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Cambio posterior de la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678365"
---
# <a name="subsequent-dvd-region-change"></a>Cambio posterior de la región de DVD

En Windows 2000 y versiones posteriores, el navegador de DVD invoca una página de propiedades en el dispositivo de unidad de DVD-ROM en el Administrador de dispositivos. Esta página de propiedades también la abre la aplicación DVDPlay.exe cuando es necesario cambiar una región. La interfaz de usuario de esta página de propiedades es muy similar a la de DVDRgn.exe y está regional en el sistema operativo.

En el caso de las unidades RPC1, los componentes del sistema operativo Windows administran los cambios de la región. Las unidades RPC2 mantienen la configuración de la región en su propio hardware. Cuando se agota el número de cambios permitidos en una unidad RPC2, la unidad no podrá realizar la llamada para cambiar la región y el componente región-cambio del sistema operativo indicará al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad de cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



