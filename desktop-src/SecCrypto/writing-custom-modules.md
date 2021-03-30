---
description: Puede escribir módulos de directivas en el lenguaje de programación C, C++ o Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Escribir módulos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002079"
---
# <a name="writing-custom-modules"></a>Escribir módulos personalizados

Puede escribir módulos de directivas en el lenguaje de programación C, C++ o Visual Basic. El compilador de Microsoft necesario está disponible en Visual C++ versión 5,0 o posterior, o en Visual Basic versión 5,0 o posterior. Una [*entidad de certificación*](../secgloss/c-gly.md) (CA) empresarial solo debe usar el módulo de directivas empresariales proporcionado por Microsoft.

Debe implementar [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) al escribir un módulo de directivas personalizado. Además, debe implementar [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) al escribir un módulo de directivas personalizado.

Los módulos de directivas pueden llamar a métodos desde [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para ayudar en el procesamiento de una [*solicitud de certificado*](../secgloss/c-gly.md). **ICertServerPolicy** permite establecer y recuperar propiedades y extensiones de certificado.

Para obtener más información, vea los siguientes temas.



| Tema                                                                      | Descripción                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [Establecer propiedades de certificado](setting-certificate-properties.md)       | Establecer las propiedades de un certificado |
| [Escribir módulos de salida personalizados](writing-custom-exit-modules.md)             | Escribir módulos de salida personalizados             |
| [Escribir controladores de extensión personalizados](writing-custom-extension-handlers.md) | Escribir controladores de extensión personalizados       |



 

 

 
