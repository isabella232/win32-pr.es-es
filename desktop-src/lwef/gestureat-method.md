---
title: Método GestureAt
description: Método GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487563"
---
# <a name="gestureat-method"></a><span data-ttu-id="00def-103">Método GestureAt</span><span class="sxs-lookup"><span data-stu-id="00def-103">GestureAt Method</span></span>

<span data-ttu-id="00def-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="00def-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="00def-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="00def-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="00def-106">Reproduce la animación gesturing para el carácter especificado en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="00def-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="00def-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="00def-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="00def-108">\*agente ***. Caracteres ("*** CharacterID \* *"). GestureAt* \*  *x, y*</span><span class="sxs-lookup"><span data-stu-id="00def-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="00def-109">Parte</span><span class="sxs-lookup"><span data-stu-id="00def-109">Part</span></span>  | <span data-ttu-id="00def-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="00def-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00def-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="00def-111">*x,y*</span></span> | <span data-ttu-id="00def-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00def-112">Required.</span></span> <span data-ttu-id="00def-113">Valor entero que indica la coordenada de pantalla horizontal (*x*) y la coordenada de pantalla vertical (*y*) a la que se moverá el carácter.</span><span class="sxs-lookup"><span data-stu-id="00def-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="00def-114">Estas coordenadas se deben especificar en píxeles.</span><span class="sxs-lookup"><span data-stu-id="00def-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00def-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00def-115">Remarks</span></span>

<span data-ttu-id="00def-116">El servidor reproduce automáticamente la animación adecuada para gestos hacia la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="00def-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="00def-117">Las coordenadas siempre se relacionan con el origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="00def-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="00def-118">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="00def-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="00def-119">Además, si la animación asociada no se ha cargado en el equipo local, el servidor establece la propiedad de [**Estado**](status-property.md) del objeto de **solicitud** en "Failed" con un número de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="00def-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="00def-120">Por consiguiente, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar las animaciones de estado de **gesturing** antes de llamar al método **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="00def-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 