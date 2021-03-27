---
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con GDI. En este tema no se proporciona todo lo que necesita saber acerca de los problemas de seguridad. En su lugar, úselo como punto de partida y referencia para esta área tecnológica.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Consideraciones de seguridad: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002409"
---
# <a name="security-considerations-gdi"></a>Consideraciones de seguridad: GDI

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con GDI. En este tema no se proporciona todo lo que necesita saber acerca de los problemas de seguridad. En su lugar, úselo como punto de partida y referencia para esta área tecnológica.

GDI generalmente tiene pocos problemas de seguridad, ya que se ocupa de mostrar en lugar de la entrada. Sin embargo, estos son algunos de los problemas que debe tener en cuenta.

Los mapas de bits, los metaarchivos y las fuentes son estructuras complejas que podrían resultar dañados. Es recomendable intentar asegurarse de que estos elementos no estén dañados y de un origen de confianza.

Una aplicación puede especificar el descriptor de seguridad para algunas de las API de impresión y puesta en cola. Debe tener cuidado al establecer el descriptor de seguridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Centro de seguridad de Microsoft](https://www.microsoft.com/security/)
</dt> <dt>

[Centro para desarrolladores de seguridad](https://technet.microsoft.com/security/)
</dt> <dt>

[TechCenter de seguridad](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



