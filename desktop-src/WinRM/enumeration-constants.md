---
title: Constantes de enumeración (WSManDisp. h)
description: La enumeración contiene constantes, como se muestra en la lista siguiente, que se usa en el parámetro flags mediante llamadas a Session. Enumerate y IWSManSession Enumerate.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422117"
---
# <a name="enumeration-constants"></a><span data-ttu-id="cf93b-103">Constantes de enumeración</span><span class="sxs-lookup"><span data-stu-id="cf93b-103">Enumeration Constants</span></span>

<span data-ttu-id="cf93b-104">La enumeración **\_ \_ WSManEnumFlags** contiene constantes, como se muestra en la lista siguiente, que se usa en el parámetro *Flags* mediante llamadas a [**Session. Enumerate**](session-enumerate.md) y [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="cf93b-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="cf93b-105">Tenga en cuenta que **WSManFlagReturnObject** y **WSManFlagHierarchyDeep** son el valor predeterminado si no se especifica el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="cf93b-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="cf93b-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="cf93b-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-107">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="cf93b-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-108">Los lotes contienen las instancias XML solicitadas.</span><span class="sxs-lookup"><span data-stu-id="cf93b-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="cf93b-109">Este es el valor predeterminado del parámetro de marca.</span><span class="sxs-lookup"><span data-stu-id="cf93b-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="cf93b-110">El método de scripting asociado es [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) y el método de C++ es [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span><span class="sxs-lookup"><span data-stu-id="cf93b-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf93b-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="cf93b-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-112">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="cf93b-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-113">Esta marca controla cómo WinRM interpreta el parámetro de *filtro* en la llamada a [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="cf93b-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="cf93b-114">El formato del filtro puede ser un fragmento XML o una cadena de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="cf93b-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="cf93b-115">El formato viene determinado por el [*dialecto de filtro*](windows-remote-management-glossary.md) del [*filtro*](windows-remote-management-glossary.md) usado en la llamada a [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), que es específico de la operación realizada.</span><span class="sxs-lookup"><span data-stu-id="cf93b-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="cf93b-116">Si no se especifica el parámetro de *dialecto* , WinRM intenta determinar el dialecto en función del primer carácter del filtro.</span><span class="sxs-lookup"><span data-stu-id="cf93b-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="cf93b-117">Si el primer carácter es <, pero el filtro no es realmente un fragmento XML, se debe establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="cf93b-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="cf93b-118">Por ejemplo, un filtro en el formato siguiente requiere que establezca **WSManFlagNonXmlText** para que el filtro se interprete correctamente:</span><span class="sxs-lookup"><span data-stu-id="cf93b-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="cf93b-119">Si el filtro es un fragmento XML, esta marca no es necesaria porque el fragmento comienza con <, que WinRM interpreta correctamente como XML.</span><span class="sxs-lookup"><span data-stu-id="cf93b-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="cf93b-120">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="cf93b-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="cf93b-121">Si el filtro está en texto sin formato que no comienza con <, esta marca no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="cf93b-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="cf93b-122">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="cf93b-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="cf93b-123">El método de scripting asociado es [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) y el método de C++ es [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span><span class="sxs-lookup"><span data-stu-id="cf93b-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf93b-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="cf93b-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-125">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="cf93b-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-126">Los lotes contienen referencias de punto de conexión (EPRs) para las instancias XML correspondientes, pero no las instancias reales.</span><span class="sxs-lookup"><span data-stu-id="cf93b-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="cf93b-127">El método de scripting asociado es [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) y el método de C++ es [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span><span class="sxs-lookup"><span data-stu-id="cf93b-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf93b-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="cf93b-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="cf93b-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-130">Los lotes contienen las instancias XML solicitadas y las EPRs correspondientes contenidas en un elemento [*wsman: items*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="cf93b-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="cf93b-131">El método de scripting asociado es [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) y el método de C++ es [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span><span class="sxs-lookup"><span data-stu-id="cf93b-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf93b-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="cf93b-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-133">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="cf93b-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-134">Las instancias de clase derivada se incluyen y se representan según sus esquemas reales.</span><span class="sxs-lookup"><span data-stu-id="cf93b-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="cf93b-135">El método de scripting asociado es [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) y el método de C++ es [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span><span class="sxs-lookup"><span data-stu-id="cf93b-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf93b-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="cf93b-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-137">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="cf93b-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-138">Se excluyen las instancias de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="cf93b-138">Derived class instances are excluded.</span></span> <span data-ttu-id="cf93b-139">Solo se muestran las instancias del tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="cf93b-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="cf93b-140">El método de scripting asociado es [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) y el método de C++ es [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span><span class="sxs-lookup"><span data-stu-id="cf93b-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf93b-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="cf93b-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf93b-142">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="cf93b-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="cf93b-143">Las instancias de clase derivada se incluyen y se representan según el esquema de la clase base.</span><span class="sxs-lookup"><span data-stu-id="cf93b-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="cf93b-144">No se muestran las propiedades definidas en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="cf93b-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="cf93b-145">El método de scripting asociado es [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) y el método de C++ es [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span><span class="sxs-lookup"><span data-stu-id="cf93b-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf93b-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf93b-146">Requirements</span></span>



| <span data-ttu-id="cf93b-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf93b-147">Requirement</span></span> | <span data-ttu-id="cf93b-148">Value</span><span class="sxs-lookup"><span data-stu-id="cf93b-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf93b-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf93b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="cf93b-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf93b-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="cf93b-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf93b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="cf93b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf93b-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cf93b-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf93b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf93b-154"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf93b-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf93b-155">IDL</span><span class="sxs-lookup"><span data-stu-id="cf93b-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf93b-156"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf93b-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf93b-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf93b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf93b-158">Constantes y enumeraciones de WinRM</span><span class="sxs-lookup"><span data-stu-id="cf93b-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="cf93b-159">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="cf93b-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="cf93b-160">Consultar instancias específicas de un recurso</span><span class="sxs-lookup"><span data-stu-id="cf93b-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





