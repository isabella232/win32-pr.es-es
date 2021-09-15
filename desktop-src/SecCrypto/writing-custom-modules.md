---
description: Puede escribir módulos de directiva en C, C++ o Visual Basic programación.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Escribir módulos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473440"
---
# <a name="writing-custom-modules"></a>Escribir módulos personalizados

Puede escribir módulos de directiva en C, C++ o Visual Basic programación. El compilador de Microsoft necesario está disponible Visual C++ versión 5.0 o posterior o Visual Basic versión 5.0 o posterior. Una entidad [*de certificación*](../secgloss/c-gly.md) (CA) empresarial debe usar solo el módulo de directivas empresariales proporcionado por Microsoft.

Debe implementar [**ICertPolicy al**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) escribir un módulo de directivas personalizadas. Además, debe implementar [**ICertManageModule al**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) escribir un módulo de directivas personalizadas.

Los módulos de directiva pueden llamar a métodos [**desde ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para ayudar en el procesamiento de una [*solicitud de certificado*](../secgloss/c-gly.md); **ICertServerPolicy permite** establecer y recuperar propiedades y extensiones de certificado.

Para obtener más información, vea los temas siguientes:



| Tema                                                                      | Descripción                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [Establecimiento de propiedades de certificado](setting-certificate-properties.md)       | Establecimiento de las propiedades de un certificado |
| [Escribir módulos de salida personalizados](writing-custom-exit-modules.md)             | Escritura de módulos de salida personalizados             |
| [Escribir controladores de extensión personalizados](writing-custom-extension-handlers.md) | Escribir controladores de extensión personalizados       |



 

 

 
