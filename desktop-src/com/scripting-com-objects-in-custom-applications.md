---
title: Scripting de objetos COM en aplicaciones personalizadas
description: Scripting de objetos COM en aplicaciones personalizadas
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268664"
---
# <a name="scripting-com-objects-in-custom-applications"></a>Scripting de objetos COM en aplicaciones personalizadas

Microsoft proporciona varios entornos para el scripting de objetos COM: páginas Active Server, Windows Script Host, etc. Los fabricantes de software independientes (ISV) también pueden conceder licencias a los motores de scripting de Microsoft para su uso en sus aplicaciones. Por ejemplo, un ISV que crea un procesador de textos podría querer agregar un lenguaje de macros a la aplicación para que los usuarios puedan automatizar las tareas sencillas. Mediante el uso de la licencia de un motor de scripting, el ISV puede usar un lenguaje como VBScript o JScript como lenguaje de macros de la aplicación.

Además de las licencias de los motores de scripting de VBScript y JScript, los ISV pueden escribir sus propios motores de scripting ActiveX. Estos motores de scripts se pueden conectar a cualquier entorno de host que admita el estándar del motor de scripting de ActiveX. Por ejemplo, un ISV puede escribir un motor de scripts de PerlScript e instalarlo en un servidor ASP, lo que permite al servidor ASP procesar scripts PerlScript.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting con objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




