---
title: Control de errores en COM (COM)
description: Control de errores en COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488902"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="b6c7f-103">Control de errores en COM (COM)</span><span class="sxs-lookup"><span data-stu-id="b6c7f-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="b6c7f-104">Casi todas las funciones COM y los métodos de interfaz devuelven un valor de tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="b6c7f-105">El **HRESULT** (para el *identificador del resultado*) es una forma de devolver valores correctos, de advertencia y de error.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="b6c7f-106">Los **Valores HRESULT** no son realmente controles de nada; solo son valores con varios campos codificados en el valor.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="b6c7f-107">Según la especificación COM, un resultado de cero indica que se ha realizado correctamente y un resultado distinto de cero indica un error.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="b6c7f-108">En el nivel de código fuente, todos los valores de error constan de tres partes, separadas por un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="b6c7f-109">La primera parte es el prefijo que identifica la instalación asociada al error, la segunda parte es E para el error y la tercera parte es una cadena que describe la condición real.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="b6c7f-110">Por ejemplo, se devuelve **STG \_ E \_ MEDIUMFULL** cuando no queda espacio en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="b6c7f-111">El prefijo **STG** indica la instalación del almacenamiento, **e** indica que el código de estado representa un error y **MEDIUMFULL** proporciona información específica sobre el error.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="b6c7f-112">Muchos de los valores que puede querer devolver desde un método de interfaz o función se definen en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b6c7f-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="b6c7f-113">Para obtener más información sobre el control de errores, vea las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="b6c7f-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="b6c7f-114">Estructura de los códigos de error COM</span><span class="sxs-lookup"><span data-stu-id="b6c7f-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="b6c7f-115">Códigos en facil \_ ITF</span><span class="sxs-lookup"><span data-stu-id="b6c7f-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="b6c7f-116">Usar macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="b6c7f-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="b6c7f-117">Control de errores COM en Java y Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b6c7f-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="b6c7f-118">Estrategias de control de errores</span><span class="sxs-lookup"><span data-stu-id="b6c7f-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="b6c7f-119">Control de errores desconocidos</span><span class="sxs-lookup"><span data-stu-id="b6c7f-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="b6c7f-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6c7f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6c7f-121">Códigos de error COM</span><span class="sxs-lookup"><span data-stu-id="b6c7f-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




