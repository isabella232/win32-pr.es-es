---
description: La propiedad locale del objeto SWbemObjectPath contiene la configuración regional de la ruta de acceso del objeto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Locale (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697358"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="65f29-103">Propiedad SWbemObjectPath. Locale</span><span class="sxs-lookup"><span data-stu-id="65f29-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="65f29-104">La propiedad **locale** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene la configuración regional de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="65f29-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="65f29-105">Cuando la propiedad **SWbemObjectPath. Locale** forma parte de un objeto [**SWbemObjectPath**](swbemobjectpath.md) independiente, es de lectura y escritura y se puede usar para establecer el componente de configuración regional del moniker.</span><span class="sxs-lookup"><span data-stu-id="65f29-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="65f29-106">Cuando se tiene acceso a la propiedad **SWbemObjectPath. Locale** como parte de una propiedad [**SWbemObject \_ . Path**](swbemobject-path-.md) , es de solo lectura y notifica el valor de la configuración regional que se usa para enlazar con el espacio de nombres desde el que se obtuvo el objeto.</span><span class="sxs-lookup"><span data-stu-id="65f29-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="65f29-107">En el caso de los identificadores de configuración regional de Microsoft, el formato de la cadena es "MS \_ xxxx", donde XXXX es una cadena en formato hexadecimal que indica el LCID.</span><span class="sxs-lookup"><span data-stu-id="65f29-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="65f29-108">Por ejemplo, el identificador de configuración regional de Inglés de Estados Unidos es "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="65f29-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="65f29-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="65f29-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="65f29-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="65f29-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f29-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65f29-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="65f29-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65f29-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="65f29-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f29-113">Requirements</span></span>



| <span data-ttu-id="65f29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f29-114">Requirement</span></span> | <span data-ttu-id="65f29-115">Value</span><span class="sxs-lookup"><span data-stu-id="65f29-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65f29-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65f29-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65f29-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65f29-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65f29-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65f29-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65f29-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65f29-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f29-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="65f29-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="65f29-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="65f29-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="65f29-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="65f29-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="65f29-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65f29-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f29-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f29-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="65f29-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="65f29-126">CLSID</span></span><br/>                    | <span data-ttu-id="65f29-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="65f29-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="65f29-128">IID</span><span class="sxs-lookup"><span data-stu-id="65f29-128">IID</span></span><br/>                      | <span data-ttu-id="65f29-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="65f29-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




