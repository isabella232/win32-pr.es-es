---
description: En esta sección se describen las macros de la utilidad Shell de Windows.
title: Macros de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002216"
---
# <a name="shell-macros"></a><span data-ttu-id="b0b08-103">Macros de Shell</span><span class="sxs-lookup"><span data-stu-id="b0b08-103">Shell Macros</span></span>

<span data-ttu-id="b0b08-104">En esta sección se describen las macros de la utilidad Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="b0b08-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0b08-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b0b08-105">In this section</span></span>



| <span data-ttu-id="b0b08-106">Tema</span><span class="sxs-lookup"><span data-stu-id="b0b08-106">Topic</span></span>                                                                  | <span data-ttu-id="b0b08-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0b08-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b08-108">**DEFINIR \_ PROPERTYKEY**</span><span class="sxs-lookup"><span data-stu-id="b0b08-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="b0b08-109">Se usa para empaquetar un identificador de formato (FMTID) y un identificador de propiedad (PID) en una estructura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) que representa una clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b0b08-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="b0b08-110">**IID \_ PPV \_ args**</span><span class="sxs-lookup"><span data-stu-id="b0b08-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="b0b08-111">Se utiliza para recuperar un puntero de interfaz, proporcionando el valor de IID de la interfaz solicitada automáticamente según el tipo de puntero de interfaz utilizado.</span><span class="sxs-lookup"><span data-stu-id="b0b08-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="b0b08-112">Esto evita un error de codificación común al comprobar el tipo del valor que se pasa en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="b0b08-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="b0b08-113">**IsEqualPropertyKey**</span><span class="sxs-lookup"><span data-stu-id="b0b08-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="b0b08-114">Compara los miembros de dos estructuras [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) y devuelve si son iguales.</span><span class="sxs-lookup"><span data-stu-id="b0b08-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="b0b08-115">**MAKEDLLVERULL**</span><span class="sxs-lookup"><span data-stu-id="b0b08-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="b0b08-116">Se usa para empaquetar la información de versión de la DLL en un valor de ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="b0b08-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="b0b08-117">**NetAddr \_ DisplayErrorTip**</span><span class="sxs-lookup"><span data-stu-id="b0b08-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="b0b08-118">Muestra un mensaje de error en el globo de sugerencias asociado con el control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="b0b08-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="b0b08-119">**NetAddr \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="b0b08-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="b0b08-120">Indica si una dirección de red se ajusta a un tipo y formato especificados.</span><span class="sxs-lookup"><span data-stu-id="b0b08-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="b0b08-121">**NetAddr \_ GetAllowType**</span><span class="sxs-lookup"><span data-stu-id="b0b08-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="b0b08-122">Recupera los tipos de dirección de red que un control de dirección de red especificado acepta.</span><span class="sxs-lookup"><span data-stu-id="b0b08-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="b0b08-123">**NetAddr \_ SetAllowType**</span><span class="sxs-lookup"><span data-stu-id="b0b08-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="b0b08-124">Establece los tipos de dirección de red que acepta un control de dirección de red especificado.</span><span class="sxs-lookup"><span data-stu-id="b0b08-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
