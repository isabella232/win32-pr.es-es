---
title: Modificar atributos con ADSI
description: Para modificar los valores de atributo, ADSI proporciona los métodos IADs. put y IADs. PutEx. Estos métodos modifican los datos en la memoria caché del lado cliente. Se debe llamar al método IADs. SetInfo para confirmar los cambios en el directorio.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modificar atributos con ADSI
- Atributos ADSI, modificar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421410"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="1d7e0-107">Modificar atributos con ADSI</span><span class="sxs-lookup"><span data-stu-id="1d7e0-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="1d7e0-108">Para modificar los valores de atributo, ADSI proporciona los métodos [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="1d7e0-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="1d7e0-109">Estos métodos modifican los datos en la memoria caché del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="1d7e0-110">Se debe llamar al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="1d7e0-111">Cuando se confirman varios cambios de atributo en una única llamada a [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), si no se puede modificar ningún atributo único, no se modificará ninguno de los atributos.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="1d7e0-112">Por ejemplo, si modifica los atributos [**SN**](/windows/desktop/ADSchema/a-sn) y [**givenName**](/windows/desktop/ADSchema/a-givenname) y borra el atributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) de un objeto User sin ninguna llamada subsiguiente al método **SetInfo** , los cambios se especifican al llamar a **SetInfo**.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="1d7e0-113">Si una o varias de las modificaciones no se permiten y, por lo tanto, no se pueden realizar, ninguna de las modificaciones colectivas realizadas en los atributos se especifican durante la llamada a **SetInfo**.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="1d7e0-114">El método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) toma un nombre de atributo y un parámetro Variant.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="1d7e0-115">Use este método para establecer los atributos que contienen valores únicos y múltiples.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="1d7e0-116">El método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) proporciona control sobre las operaciones en atributos con varios valores.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="1d7e0-117">Puede anexar, eliminar, actualizar y borrar valores existentes.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="1d7e0-118">El método **IADs. PutEx** siempre espera una matriz de valores de atributo Variant.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="1d7e0-119">Sin embargo, puede utilizar este método para establecer un atributo con un solo valor.</span><span class="sxs-lookup"><span data-stu-id="1d7e0-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="1d7e0-120">El método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa las operaciones especificadas por la enumeración de la enumeración de la operación de la [**\_ propiedad \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="1d7e0-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 