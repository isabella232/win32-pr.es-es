---
description: Control de Unicode en una aplicación IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Control de Unicode en una aplicación IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688712"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="ff9a4-103">Control de Unicode en una aplicación IME-Aware</span><span class="sxs-lookup"><span data-stu-id="ff9a4-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="ff9a4-104">Dos problemas están relacionados con el IMM y su control de Unicode.</span><span class="sxs-lookup"><span data-stu-id="ff9a4-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="ff9a4-105">El primer problema es que las versiones Unicode de las funciones de IMM recuperan el tamaño de un búfer en bytes en lugar de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ff9a4-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="ff9a4-106">El segundo problema es que el IMM normalmente recupera caracteres Unicode (en lugar de caracteres DBCS) en los mensajes [**WM \_ Char**](../inputdev/wm-char.md) y [**WM \_ IME \_ Char**](wm-ime-char.md) .</span><span class="sxs-lookup"><span data-stu-id="ff9a4-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="ff9a4-107">Windows admite una interfaz Unicode para el IMM, además de la interfaz ANSI admitida originalmente.</span><span class="sxs-lookup"><span data-stu-id="ff9a4-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="ff9a4-108">Las aplicaciones deben usar [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) para que los mensajes de char de [**WM \_ Char**](../inputdev/wm-char.md) y [**WM \_ IME \_**](wm-ime-char.md) recuperen caracteres Unicode en lugar de caracteres DBCS en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ff9a4-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff9a4-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff9a4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff9a4-110">Usar el administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ff9a4-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
