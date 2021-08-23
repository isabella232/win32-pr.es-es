---
description: Dado que Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para grupos de usuarios determinados mediante la aplicación de operaciones de transformación al paquete.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ece84afd2b9ca5ce547d9ea96aed23786f78c89f01f5b5b5eaa78e2791e86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947859"
---
# <a name="customization"></a>Personalización

Dado que Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para grupos de usuarios determinados mediante la aplicación de operaciones de transformación al paquete. Las transformaciones se pueden usar para encapsular las distintas personalizaciones de un paquete base que requieren los distintos grupos de trabajo. Para obtener más información, [vea Merges and Transforms](merges-and-transforms.md).

Se pueden aplicar varias transformaciones de un paquete base sobre la marcha durante la instalación. Esto proporciona un mecanismo para asignar eficazmente instalaciones personalizadas a diferentes grupos de usuarios. Por ejemplo, esto sería útil en organizaciones en las que los departamentos de finanzas y personal de soporte técnico requieren instalaciones diferentes de un producto determinado. El producto puede estar disponible para todos los usuarios de la organización mediante una [instalación](administrative-installation.md) administrativa del paquete base en un único punto de instalación administrativa. Cada grupo de trabajo puede recibir automáticamente su personalización adecuada mediante una transformación sobre la marcha al instalar el producto.

 

 



