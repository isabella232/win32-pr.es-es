---
description: Para quitar una aplicación que se ha instalado en el estado anunciado, basta con desinstalarla mediante MsiInstallProduct o MsiConfigureProduct. También puede quitar una aplicación anunciada de la línea de comandos. Vea Opciones de la línea de comandos.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Quitar una aplicación anunciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880ce7d7de7ce7a8f9c9a20511f3f9d1b48ccdf34ffd2da51a71d226d0770b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041585"
---
# <a name="removing-an-advertised-application"></a>Quitar una aplicación anunciada

Para quitar una aplicación que se ha instalado en el estado anunciado, simplemente desinstale mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) [**o MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). También puede quitar una aplicación anunciada de la línea de comandos. Vea [Opciones de la línea de comandos](command-line-options.md).

Tenga en cuenta que es posible que no pueda quitar una aplicación anunciada si ha escrito el paquete de forma que la ejecución de una instalación esté condicional a la instrucción **NOT Installed**. Una aplicación anunciada no está instalada en el equipo del usuario y el instalador no establece [**la propiedad Instalada.**](installed.md) El paquete debe crearse para que se puedan desinstalar las aplicaciones anunciadas.

 

 



