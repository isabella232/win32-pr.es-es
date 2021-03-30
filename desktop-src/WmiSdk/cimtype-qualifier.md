---
description: El calificador CIMType contiene texto que describe el tipo de una propiedad.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Calificador CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156829"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="aa837-103">Calificador CIMType</span><span class="sxs-lookup"><span data-stu-id="aa837-103">CIMType Qualifier</span></span>

<span data-ttu-id="aa837-104">El calificador **CIMType** contiene texto que describe el tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="aa837-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="aa837-105">Este texto puede ser el tipo MOF, como "String" y "sint32", o el tipo CIM, como "CIM \_ String" y "CIM \_ sint32".</span><span class="sxs-lookup"><span data-stu-id="aa837-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="aa837-106">Hay una correspondencia uno a uno entre el calificador **CIMType** y el tipo de la propiedad que se usa en el parámetro *PvtType* del método [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="aa837-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="aa837-107">Las dos excepciones son:</span><span class="sxs-lookup"><span data-stu-id="aa837-107">The two exceptions are:</span></span>

-   <span data-ttu-id="aa837-108">[*Propiedades de referencia*](gloss-r.md), que tienen el tipo de **\_ referencia CIM**, que contiene el valor "Ref: className".</span><span class="sxs-lookup"><span data-stu-id="aa837-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="aa837-109">El valor className describe el tipo de clase de la propiedad Reference.</span><span class="sxs-lookup"><span data-stu-id="aa837-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="aa837-110">Propiedades de objeto incrustado, que tienen el tipo de **\_ objeto CIM** .</span><span class="sxs-lookup"><span data-stu-id="aa837-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="aa837-111">Sin embargo, tenga en cuenta que el calificador **CIMType** puede y debe usarse para escribir una propiedad de referencia más exactamente.</span><span class="sxs-lookup"><span data-stu-id="aa837-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="aa837-112">Por ejemplo, si la propiedad siempre hace referencia a las instancias de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , su calificador **CIMType** debe establecerse en:</span><span class="sxs-lookup"><span data-stu-id="aa837-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="aa837-113">De forma predeterminada, el calificador **CIMType** de una propiedad de referencia tiene el tipo **ref**.</span><span class="sxs-lookup"><span data-stu-id="aa837-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="aa837-114">Al igual que con las propiedades de referencia, el calificador **CIMType** debe usarse para escribir una propiedad de objeto incrustado más exactamente con la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="aa837-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="aa837-115">Dado que WMI permite más tipos de los que se pueden expresar mediante constantes estándar con el \_ prefijo VT, el calificador **CIMType** puede ayudar a interpretar los valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="aa837-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="aa837-116">El calificador **CIMType** se agrega automáticamente.</span><span class="sxs-lookup"><span data-stu-id="aa837-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="aa837-117">Para obtener más información, vea [tipos de datos MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="aa837-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa837-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa837-118">Requirements</span></span>



| <span data-ttu-id="aa837-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa837-119">Requirement</span></span> | <span data-ttu-id="aa837-120">Value</span><span class="sxs-lookup"><span data-stu-id="aa837-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="aa837-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa837-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa837-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa837-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="aa837-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa837-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa837-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa837-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa837-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa837-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa837-126">**Calificadores WMI estándar**</span><span class="sxs-lookup"><span data-stu-id="aa837-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="aa837-127">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="aa837-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="aa837-128">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="aa837-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

