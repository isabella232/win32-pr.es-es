---
description: Dado que el Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para determinados grupos de usuarios mediante la aplicación de operaciones de transformación al paquete.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666587"
---
# <a name="customization"></a>Personalización

Dado que el Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para determinados grupos de usuarios mediante la aplicación de operaciones de transformación al paquete. Las transformaciones se pueden usar para encapsular las diferentes personalizaciones de un paquete base que requieren grupos de trabajo diferentes. Para obtener más información, vea [combinaciones y transformaciones](merges-and-transforms.md).

Se pueden aplicar varias transformaciones de un paquete base sobre la marcha durante la instalación. Esto proporciona un mecanismo para asignar eficazmente instalaciones personalizadas a distintos grupos de usuarios. Por ejemplo, esto sería útil en organizaciones en las que los departamentos de soporte técnico y Finanzas requieren diferentes instalaciones de un producto determinado. El producto puede ponerse a disposición de todos los usuarios de la organización mediante una [instalación administrativa](administrative-installation.md) del paquete base en un único punto de instalación administrativa. A continuación, cada grupo de trabajo puede recibir automáticamente su personalización adecuada por medio de una transformación sobre la marcha al instalar el producto.

 

 



