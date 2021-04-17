---
description: .
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Control de versiones (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2da50dae53fd2309f1a5de10996c57a2b4ac29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707493"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Control de versiones (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)

Uno de los problemas de compatibilidad de aplicaciones más comunes para Windows Internet Explorer son las cadenas de agente de usuario (UA) y los vectores de versión. Windows Internet Explorer 8 introduce una nueva cadena de UA para ayudar a las aplicaciones a detectar qué versión están ejecutando los usuarios. Además de simplemente aumentar el valor de MSIE que está asociado con Internet Explorer en la cadena UA, Internet Explorer 8 agrega un valor Trident/4.0 para ayudarle a detectar si Internet Explorer 8 se está ejecutando en modo de vista de compatibilidad. Estos cambios, además de las comprobaciones de versión codificadas, pueden introducir problemas de compatibilidad entre exploradores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualizaciones de diseño que afectan a la compatibilidad entre exploradores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



