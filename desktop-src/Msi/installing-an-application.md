---
description: Puede instalar productos completos con las Windows installer. En los pasos siguientes se describe cómo instalar un producto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Instalación de una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aad6e130d78bd30b940232aeb6fe1da6508be754fe50b9abb9dbcaa0186562
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327965"
---
# <a name="installing-an-application"></a>Instalación de una aplicación

Puede instalar productos completos con las Windows installer. En los pasos siguientes se describe cómo instalar un producto.

**Para instalar un producto**

1.  Ejecute un producto a través de su secuencia de instalación o desinstalación mediante una llamada a [**la función MsiInstallProduct.**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
2.  Especifique el nivel de instalación mediante una llamada a [**la función MsiConfigureProduct.**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)

    Puede usar los parámetros de la función [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) para establecer el estado de instalación. Por ejemplo, puede establecer el estado para instalar localmente o para instalar desde el origen. Puede establecer el intervalo de características del producto que se incluirá estableciendo el nivel .

Para obtener más información sobre cómo instalar una aplicación, vea [Resistencia y](resiliency.md) mecanismo [de instalación](installation-mechanism.md).

 

 



