---
description: Para quitar una aplicación que se ha instalado en el estado anunciado, simplemente desinstálelo mediante MsiInstallProduct o MsiConfigureProduct. También puede quitar una aplicación anunciada de la línea de comandos. Vea opciones de la línea de comandos.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Quitar una aplicación anunciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910694"
---
# <a name="removing-an-advertised-application"></a>Quitar una aplicación anunciada

Para quitar una aplicación que se ha instalado en el estado anunciado, simplemente desinstálelo mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). También puede quitar una aplicación anunciada de la línea de comandos. Vea [Opciones](command-line-options.md)de la línea de comandos.

Tenga en cuenta que es posible que no pueda quitar una aplicación anunciada si ha creado el paquete de forma que la ejecución de una instalación sea condicional en la instrucción **no instalada**. Una aplicación anunciada no está instalada en el equipo del usuario y el instalador no establece la propiedad [**instalado**](installed.md) . Se debe crear el paquete para que se puedan desinstalar las aplicaciones anunciadas.

 

 



