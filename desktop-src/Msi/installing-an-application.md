---
description: Puede instalar productos completos con las Windows Installer. En los pasos siguientes se describe cómo instalar un producto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Instalación de una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072056"
---
# <a name="installing-an-application"></a>Instalación de una aplicación

Puede instalar productos completos con las Windows Installer. En los pasos siguientes se describe cómo instalar un producto.

**Para instalar un producto**

1.  Ejecute un producto a través de su secuencia de instalación o desinstalación mediante una llamada a [**la función MsiInstallProduct.**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
2.  Especifique el nivel de instalación mediante una llamada a [**la función MsiConfigureProduct.**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)

    Puede usar los parámetros de la función [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) para establecer el estado de instalación. Por ejemplo, puede establecer el estado para instalar localmente o para instalar desde el origen. Puede establecer el intervalo de características del producto que se incluirá estableciendo el nivel .

Para obtener más información sobre cómo instalar una aplicación, vea [Resistencia y](resiliency.md) mecanismo [de instalación](installation-mechanism.md).

 

 



