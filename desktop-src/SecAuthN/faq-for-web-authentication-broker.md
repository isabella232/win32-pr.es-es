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
# <a name="faq-for-web-authentication-broker"></a><span data-ttu-id="ee56c-103">Preguntas más frecuentes sobre el agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="ee56c-103">FAQ for Web Authentication Broker</span></span>

<span data-ttu-id="ee56c-104">Preguntas más frecuentes sobre el agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="ee56c-104">Frequently asked questions for Web Authentication Broker.</span></span>



| <span data-ttu-id="ee56c-105">Pregunta</span><span class="sxs-lookup"><span data-stu-id="ee56c-105">Question</span></span>                                                                                                    | <span data-ttu-id="ee56c-106">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee56c-106">Answer</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee56c-107">¿Cómo puedo asegurarme de que mi página de https://funciona con el agente de autenticación Web?</span><span class="sxs-lookup"><span data-stu-id="ee56c-107">How can I make sure that my https:// page works with the Web Authentication Broker?</span></span>                         | <span data-ttu-id="ee56c-108">Intente cargar la página en Windows Internet Explorer antes de intentarlo con el agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="ee56c-108">Try loading the page in Windows Internet Explorer before trying it with Web Authentication Broker.</span></span> <span data-ttu-id="ee56c-109">Si la página web se carga sin errores, también se representará correctamente en el agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="ee56c-109">If your web page loads with no errors, it will be rendered correctly by the Web Authentication Broker as well.</span></span> |
| <span data-ttu-id="ee56c-110">En caso de error, ¿se mostrarán al usuario los códigos de error?</span><span class="sxs-lookup"><span data-stu-id="ee56c-110">In case of an error, will the error codes be displayed to the user?</span></span>                                         | <span data-ttu-id="ee56c-111">Mientras se muestre una página de error al usuario, no se muestra el código de error subyacente.</span><span class="sxs-lookup"><span data-stu-id="ee56c-111">While an error page will be displayed to the user, the underlying error code is not shown.</span></span> <span data-ttu-id="ee56c-112">Solo se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee56c-112">It is only returned to the app.</span></span> <span data-ttu-id="ee56c-113">Como alternativa, también puede usar los registros operativos.</span><span class="sxs-lookup"><span data-stu-id="ee56c-113">Alternately, you can also use the operational logs.</span></span>                                    |
| <span data-ttu-id="ee56c-114">¿Cómo puedo encontrar más detalles sobre el error encontrado?</span><span class="sxs-lookup"><span data-stu-id="ee56c-114">How can I find more details on the error encountered?</span></span>                                                       | <span data-ttu-id="ee56c-115">Use los registros operativos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ee56c-115">Use the operational logs for details.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="ee56c-116">¿El contenedor de la aplicación de inicio de sesión único (SSO) comparte sus cookies con Internet Explorer u otros exploradores?</span><span class="sxs-lookup"><span data-stu-id="ee56c-116">Does the single sign-on (SSO) app container share its cookies with the Internet Explorer or other browsers?</span></span> | <span data-ttu-id="ee56c-117">No.</span><span class="sxs-lookup"><span data-stu-id="ee56c-117">No.</span></span>                                                                                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ee56c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee56c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee56c-119">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="ee56c-119">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="ee56c-120">Aplicación de ejemplo del SDK del agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="ee56c-120">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="ee56c-121">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="ee56c-121">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
