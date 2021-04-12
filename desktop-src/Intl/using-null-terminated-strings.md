---
description: Las aplicaciones Unicode siempre deben convertir cero en TCHAR al usar cadenas terminadas en NULL.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Usar cadenas terminadas en null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279493"
---
# <a name="using-null-terminated-strings"></a><span data-ttu-id="6fa11-103">Usar cadenas terminadas en null</span><span class="sxs-lookup"><span data-stu-id="6fa11-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="6fa11-104">Las aplicaciones Unicode siempre deben convertir cero en TCHAR al usar cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="6fa11-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="6fa11-105">El código 0x0000 es el terminador de cadena Unicode para una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="6fa11-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="6fa11-106">Un solo byte nulo no es suficiente para este código, ya que muchos caracteres Unicode contienen bytes NULL como byte alto o bajo.</span><span class="sxs-lookup"><span data-stu-id="6fa11-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="6fa11-107">Un ejemplo es la letra A, para la que el código de carácter es 0x0041.</span><span class="sxs-lookup"><span data-stu-id="6fa11-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fa11-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fa11-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fa11-109">Usar caracteres especiales en Unicode</span><span class="sxs-lookup"><span data-stu-id="6fa11-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



