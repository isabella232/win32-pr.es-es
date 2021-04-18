---
description: Puede filtrar las instancias de una clase de vista de combinación asignando una consulta WQL al calificador PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Calificador PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706753"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="c9b2a-103">Calificador PostJoinFilter</span><span class="sxs-lookup"><span data-stu-id="c9b2a-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="c9b2a-104">Puede filtrar las instancias de una clase de vista de combinación asignando una consulta WQL al calificador **PostJoinFilter** .</span><span class="sxs-lookup"><span data-stu-id="c9b2a-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="c9b2a-105">El valor de la consulta WQL se aplica a las instancias de la clase de vista join.</span><span class="sxs-lookup"><span data-stu-id="c9b2a-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="c9b2a-106">Puede utilizar este calificador para restringir las instancias de la clase de vista a aquellas que cumplan condiciones específicas.</span><span class="sxs-lookup"><span data-stu-id="c9b2a-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="c9b2a-107">La consulta WQL siguiente filtra las instancias de una clase de combinación llamadas basadas en instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="c9b2a-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="c9b2a-108">Existen varias restricciones en el uso de este calificador:</span><span class="sxs-lookup"><span data-stu-id="c9b2a-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="c9b2a-109">**PostJoinFilter** solo está disponible para las clases de vista de combinación.</span><span class="sxs-lookup"><span data-stu-id="c9b2a-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="c9b2a-110">El nombre de clase y los nombres de propiedad especificados en la consulta hacen referencia a las propiedades de la clase de vista, no a la clase de origen.</span><span class="sxs-lookup"><span data-stu-id="c9b2a-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="c9b2a-111">No se permite la exclusión de propiedades; solo `SELECT *` se permiten consultas de tipo.</span><span class="sxs-lookup"><span data-stu-id="c9b2a-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b2a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9b2a-112">Requirements</span></span>



| <span data-ttu-id="c9b2a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b2a-113">Requirement</span></span> | <span data-ttu-id="c9b2a-114">Value</span><span class="sxs-lookup"><span data-stu-id="c9b2a-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c9b2a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9b2a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b2a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9b2a-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c9b2a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9b2a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b2a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9b2a-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9b2a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9b2a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b2a-120">**Calificadores específicos del proveedor de vistas**</span><span class="sxs-lookup"><span data-stu-id="c9b2a-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

