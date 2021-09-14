---
description: Dado que Windows Installer conserva toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para grupos de usuarios determinados mediante la aplicación de operaciones de transformación al paquete.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158664"
---
# <a name="customization"></a>Personalización

Dado que Windows Installer conserva toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para grupos de usuarios determinados mediante la aplicación de operaciones de transformación al paquete. Las transformaciones se pueden usar para encapsular las distintas personalizaciones de un paquete base que requieren los distintos grupos de trabajo. Para obtener más información, [vea Merges and Transforms](merges-and-transforms.md).

Se pueden aplicar varias transformaciones de un paquete base sobre la marcha durante la instalación. Esto proporciona un mecanismo para asignar eficazmente instalaciones personalizadas a diferentes grupos de usuarios. Por ejemplo, esto sería útil en organizaciones en las que los departamentos de finanzas y personal de soporte técnico requieren instalaciones diferentes de un producto determinado. El producto puede estar disponible para todos los usuarios de la organización mediante una [instalación](administrative-installation.md) administrativa del paquete base en un único punto de instalación administrativa. Cada grupo de trabajo puede recibir automáticamente su personalización adecuada mediante una transformación sobre la marcha al instalar el producto.

 

 



