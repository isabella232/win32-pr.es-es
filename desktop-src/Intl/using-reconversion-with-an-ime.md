---
description: Un IME implementa una característica llamada &\# 0034; reconversión&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Usar la reconversión con un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677262"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="b26dd-103">Usar la reconversión con un IME</span><span class="sxs-lookup"><span data-stu-id="b26dd-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="b26dd-104">Un IME implementa una característica denominada "reconversión".</span><span class="sxs-lookup"><span data-stu-id="b26dd-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="b26dd-105">Normalmente, el IMM determina las listas de candidatos basándose solo en las entradas escritas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b26dd-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="b26dd-106">La reconversión permite al IMM determinar uno o más candidatos en función de la oración que lo contiene (el contexto).</span><span class="sxs-lookup"><span data-stu-id="b26dd-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="b26dd-107">Los tipos de conversión definidos son simple, normal y mejorado.</span><span class="sxs-lookup"><span data-stu-id="b26dd-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="b26dd-108">La reconversión resulta útil cuando un usuario observa un error de composición en un documento.</span><span class="sxs-lookup"><span data-stu-id="b26dd-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="b26dd-109">El usuario puede seleccionar el error y elegir reconversión en un menú.</span><span class="sxs-lookup"><span data-stu-id="b26dd-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="b26dd-110">El IME usa el contexto para determinar el mejor reemplazo.</span><span class="sxs-lookup"><span data-stu-id="b26dd-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="b26dd-111">La aplicación puede utilizar [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) para admitir la reconversión.</span><span class="sxs-lookup"><span data-stu-id="b26dd-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b26dd-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b26dd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b26dd-113">Usar el administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b26dd-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



