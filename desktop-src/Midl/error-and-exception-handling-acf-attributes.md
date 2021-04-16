---
title: Atributos ACF de control de errores y excepciones
description: Utilice los siguientes atributos para el control de errores.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- Los MIDL, atributos, errores y control de excepciones de ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685708"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="43161-104">Atributos ACF de control de errores y excepciones</span><span class="sxs-lookup"><span data-stu-id="43161-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="43161-105">Utilice los siguientes atributos para el control de errores.</span><span class="sxs-lookup"><span data-stu-id="43161-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="43161-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="43161-106">Attribute</span></span>                                                                | <span data-ttu-id="43161-107">Uso</span><span class="sxs-lookup"><span data-stu-id="43161-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43161-108">Estado de error de [**\_ Estado de comunicación**](comm-status.md)[**\_**](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="43161-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="43161-109">Permita que la aplicación cliente controle las excepciones correctamente provocando que los errores del servidor y la comunicación se devuelvan al cliente como valores de parámetro.</span><span class="sxs-lookup"><span data-stu-id="43161-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="43161-110">A continuación, la aplicación cliente puede llamar a la función de tiempo de ejecución de RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) para retransmitir un mensaje de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="43161-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43161-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43161-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43161-112">Importar archivos y bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="43161-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 