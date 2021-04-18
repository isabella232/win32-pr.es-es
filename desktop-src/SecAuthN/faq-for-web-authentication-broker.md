---
description: Preguntas más frecuentes sobre el agente de autenticación Web.
ms.assetid: 49ACB2E3-CF57-4D8E-9670-E7C18A06F76A
title: Preguntas más frecuentes sobre el agente de autenticación Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95942a32bba86f7b2ccb12264cc1a50419b248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545891"
---
# <a name="faq-for-web-authentication-broker"></a>Preguntas más frecuentes sobre el agente de autenticación Web

Preguntas más frecuentes sobre el agente de autenticación Web.



| Pregunta                                                                                                    | Respuesta                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ¿Cómo puedo asegurarme de que mi página de https://funciona con el agente de autenticación Web?                         | Intente cargar la página en Windows Internet Explorer antes de intentarlo con el agente de autenticación Web. Si la página web se carga sin errores, también se representará correctamente en el agente de autenticación Web. |
| En caso de error, ¿se mostrarán al usuario los códigos de error?                                         | Mientras se muestre una página de error al usuario, no se muestra el código de error subyacente. Solo se devuelve a la aplicación. Como alternativa, también puede usar los registros operativos.                                    |
| ¿Cómo puedo encontrar más detalles sobre el error encontrado?                                                       | Use los registros operativos para obtener más información.                                                                                                                                                                             |
| ¿El contenedor de la aplicación de inicio de sesión único (SSO) comparte sus cookies con Internet Explorer u otros exploradores? | No.                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
