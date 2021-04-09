---
description: 'Puede definir ámbitos de entrada personalizados usando modelos de lenguaje compuestos por expresiones regulares para escritura a mano y asignándoles los campos. Por ejemplo, si va a crear una aplicación de base de datos para los elementos de almacén y desea que los usuarios puedan escribir números de pieza con el panel de escritura del panel de entrada de Tablet PC. Si la sintaxis del número de pieza consta de tres letras seguidos de cuatro números seguidos de otra letra (por ejemplo, ABC1234D), el reconocedor de escritura a mano tendría un tiempo difícil para reconocer dicha entrada porque no está definida en el modelo de lenguaje. No hay ningún Factoid predefinido que se corresponda con dicha sintaxis, ni Microsoft puede incluir la sintaxis de cada campo posible que una aplicación pueda necesitar. Las expresiones regulares de escritura a mano proporcionan una forma sencilla de que las aplicaciones definan su propio modelo de lenguaje para un campo de uso especial determinado. Nota: cuando se trabaja en una aplicación habilitada para tinta que usa la propiedad Factoid del objeto RecognizerContext, no se puede usar la versión 1 Factoids en una expresión regular.'
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Ámbitos de entrada personalizados con expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080302"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="3840d-106">Ámbitos de entrada personalizados con expresiones regulares</span><span class="sxs-lookup"><span data-stu-id="3840d-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="3840d-107">Puede definir ámbitos de entrada personalizados usando modelos de lenguaje compuestos por expresiones regulares para escritura a mano y asignándoles los campos.</span><span class="sxs-lookup"><span data-stu-id="3840d-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="3840d-108">Por ejemplo, si va a crear una aplicación de base de datos para los elementos de almacén y desea que los usuarios puedan escribir números de pieza con el panel de escritura del panel de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3840d-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="3840d-109">Si la sintaxis del número de pieza consta de tres letras seguidos de cuatro números seguidos de otra letra (por ejemplo, ABC1234D), el reconocedor de escritura a mano tendría un tiempo difícil para reconocer dicha entrada porque no está definida en el modelo de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="3840d-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="3840d-110">No hay ningún Factoid predefinido que se corresponda con dicha sintaxis, ni Microsoft puede incluir la sintaxis de cada campo posible que una aplicación pueda necesitar.</span><span class="sxs-lookup"><span data-stu-id="3840d-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="3840d-111">Las expresiones regulares de escritura a mano proporcionan una forma sencilla de que las aplicaciones definan su propio modelo de lenguaje para un campo de uso especial determinado.</span><span class="sxs-lookup"><span data-stu-id="3840d-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="3840d-112">Cuando se trabaja en una aplicación habilitada para tinta que usa la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) , no se puede usar la versión 1 Factoids en una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="3840d-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



