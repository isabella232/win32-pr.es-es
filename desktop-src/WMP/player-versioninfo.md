---
title: Player. versionInfo
description: La propiedad versionInfo recupera un valor de cadena que especifica la versión de Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Media Player de Windows Player. versionInfo
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708756"
---
# <a name="playerversioninfo"></a><span data-ttu-id="4836b-104">Player. versionInfo</span><span class="sxs-lookup"><span data-stu-id="4836b-104">Player.versionInfo</span></span>

<span data-ttu-id="4836b-105">La propiedad **versionInfo** recupera un valor de cadena que especifica la versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4836b-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="4836b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4836b-106">Syntax</span></span>

<span data-ttu-id="4836b-107">*reproductor* . **versionInfo**</span><span class="sxs-lookup"><span data-stu-id="4836b-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4836b-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4836b-108">Possible Values</span></span>

<span data-ttu-id="4836b-109">Esta propiedad es una **cadena** de solo lectura con el siguiente formato: "*X*. 0,0. *Yyyy*", donde *X* representa el número de versión principal e *yyyy* representa el número de compilación.</span><span class="sxs-lookup"><span data-stu-id="4836b-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="4836b-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4836b-110">Examples</span></span>

<span data-ttu-id="4836b-111">En el ejemplo siguiente se crea un elemento de botón HTML que, cuando se hace clic en él, muestra un cuadro de mensaje que contiene la información de versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4836b-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="4836b-112">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4836b-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="4836b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4836b-113">Requirements</span></span>



| <span data-ttu-id="4836b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4836b-114">Requirement</span></span> | <span data-ttu-id="4836b-115">Value</span><span class="sxs-lookup"><span data-stu-id="4836b-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4836b-116">Versión</span><span class="sxs-lookup"><span data-stu-id="4836b-116">Version</span></span><br/> | <span data-ttu-id="4836b-117">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4836b-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4836b-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4836b-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="4836b-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4836b-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4836b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4836b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4836b-121">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="4836b-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





