---
description: Devuelve una representación XML de un objeto o una instancia. Se da formato al archivo de texto en el formato XML especificado como se muestra en WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Método SWbemObjectEx.GetText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083337"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="be3c2-104">SWbemObjectEx. GetText ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="be3c2-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="be3c2-105">El **método \_ gettext** del objeto [**SWBEMOBJECTEX**](swbemobjectex.md) devuelve una representación XML de un objeto o una instancia.</span><span class="sxs-lookup"><span data-stu-id="be3c2-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="be3c2-106">Se da formato al archivo de texto en el formato XML especificado como se muestra en [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span><span class="sxs-lookup"><span data-stu-id="be3c2-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="be3c2-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="be3c2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be3c2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be3c2-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="be3c2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be3c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3c2-110">*iTextFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be3c2-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="be3c2-111">Required.</span></span> <span data-ttu-id="be3c2-112">Un valor de [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) que especifica el formato XML resultante.</span><span class="sxs-lookup"><span data-stu-id="be3c2-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="be3c2-113">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="be3c2-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-114">Marcas de operación reservadas.</span><span class="sxs-lookup"><span data-stu-id="be3c2-114">Reserved operation flags.</span></span> <span data-ttu-id="be3c2-115">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="be3c2-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="be3c2-116">*objWbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="be3c2-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-117">Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que establece el contexto de la operación.</span><span class="sxs-lookup"><span data-stu-id="be3c2-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="be3c2-118">El valor predeterminado es null.</span><span class="sxs-lookup"><span data-stu-id="be3c2-118">The default is null.</span></span> <span data-ttu-id="be3c2-119">Para obtener más información sobre los pares de nombre/valor permitidos, vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="be3c2-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3c2-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be3c2-120">Return value</span></span>

<span data-ttu-id="be3c2-121">Este método no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="be3c2-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="be3c2-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="be3c2-122">Error codes</span></span>

<span data-ttu-id="be3c2-123">Después de completar el **método \_ gettext** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="be3c2-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="be3c2-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="be3c2-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="be3c2-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="be3c2-126">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="be3c2-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-127">No se encontró el formato solicitado.</span><span class="sxs-lookup"><span data-stu-id="be3c2-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="be3c2-128">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="be3c2-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-129">Uno de los parámetros de la llamada no es correcto.</span><span class="sxs-lookup"><span data-stu-id="be3c2-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="be3c2-130">**wbemErrCriticalError** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="be3c2-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="be3c2-131">Se produjo un error interno, grave e inesperado.</span><span class="sxs-lookup"><span data-stu-id="be3c2-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="be3c2-132">Comunique este error al Servicio de soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="be3c2-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be3c2-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be3c2-133">Remarks</span></span>

<span data-ttu-id="be3c2-134">Al construir [**SWbemNamedValueSet**](swbemnamedvalueset.md), solo se permiten los siguientes pares de nombre/valor.</span><span class="sxs-lookup"><span data-stu-id="be3c2-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be3c2-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="be3c2-135">Name</span></span></th>
<th><span data-ttu-id="be3c2-136">Value</span><span class="sxs-lookup"><span data-stu-id="be3c2-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be3c2-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="be3c2-137">LocalOnly</span></span></td>
<td><span data-ttu-id="be3c2-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="be3c2-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="be3c2-139">Si <strong>es true</strong>, solo las propiedades y los métodos definidos localmente están presentes en el XML resultante.</span><span class="sxs-lookup"><span data-stu-id="be3c2-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="be3c2-140">El valor predeterminado es <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="be3c2-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be3c2-141">IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="be3c2-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="be3c2-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="be3c2-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="be3c2-143">Si <strong>es true</strong>, los calificadores de clases, instancias, propiedades y métodos se incluyen en el XML resultante.</span><span class="sxs-lookup"><span data-stu-id="be3c2-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="be3c2-144">El valor predeterminado es <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="be3c2-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be3c2-145">PathLevel</span><span class="sxs-lookup"><span data-stu-id="be3c2-145">PathLevel</span></span></td>
<td><span data-ttu-id="be3c2-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="be3c2-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="be3c2-147">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="be3c2-147">Default is 0 (zero).</span></span> <span data-ttu-id="be3c2-148">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="be3c2-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="be3c2-149">0: <CLASS> <INSTANCE> se crea un elemento o en función de si el objeto es una clase o una instancia.</span><span class="sxs-lookup"><span data-stu-id="be3c2-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="be3c2-150">1: <VALUE.NAMEDOBJECT> se genera un elemento.</span><span class="sxs-lookup"><span data-stu-id="be3c2-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="be3c2-151">2: <VALUE.OBJECTWITHLOCALPATH> se genera un elemento.</span><span class="sxs-lookup"><span data-stu-id="be3c2-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="be3c2-152">3: <VALUE.OBJECTWITHPATH> se genera un elemento.</span><span class="sxs-lookup"><span data-stu-id="be3c2-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be3c2-153">ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="be3c2-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="be3c2-154"><strong>VT-BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="be3c2-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="be3c2-155">Si <strong>es true</strong>, las propiedades del sistema, como __NAMESPACE, se excluyen de la salida.</span><span class="sxs-lookup"><span data-stu-id="be3c2-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be3c2-156">IncludeClassOrigin</span><span class="sxs-lookup"><span data-stu-id="be3c2-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="be3c2-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="be3c2-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="be3c2-158">Si es <strong>true</strong>, se establece el atributo de origen de clase en los <PROPERTY> <METHOD> elementos y.</span><span class="sxs-lookup"><span data-stu-id="be3c2-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="be3c2-159">El valor predeterminado es <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="be3c2-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="be3c2-160">Para obtener más información sobre cómo crear un [**SWbemNamedValueSet**](swbemnamedvalueset.md), vea [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).</span><span class="sxs-lookup"><span data-stu-id="be3c2-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="be3c2-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="be3c2-161">Examples</span></span>

<span data-ttu-id="be3c2-162">El siguiente script muestra cómo obtener una representación XML de la definición de clase de [**\_ BIOS de Win32**](/windows/desktop/CIMWin32Prov/win32-bios) .</span><span class="sxs-lookup"><span data-stu-id="be3c2-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="be3c2-163">Al especificar una instancia concreta del **\_ BIOS de Win32**, puede obtener los datos de ese objeto en XML.</span><span class="sxs-lookup"><span data-stu-id="be3c2-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="be3c2-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be3c2-164">Requirements</span></span>



| <span data-ttu-id="be3c2-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="be3c2-165">Requirement</span></span> | <span data-ttu-id="be3c2-166">Value</span><span class="sxs-lookup"><span data-stu-id="be3c2-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be3c2-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be3c2-167">Minimum supported client</span></span><br/> | <span data-ttu-id="be3c2-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be3c2-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be3c2-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be3c2-169">Minimum supported server</span></span><br/> | <span data-ttu-id="be3c2-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be3c2-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be3c2-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be3c2-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="be3c2-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be3c2-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="be3c2-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="be3c2-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="be3c2-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="be3c2-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="be3c2-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be3c2-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be3c2-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be3c2-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="be3c2-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="be3c2-177">CLSID</span></span><br/>                    | <span data-ttu-id="be3c2-178">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="be3c2-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="be3c2-179">IID</span><span class="sxs-lookup"><span data-stu-id="be3c2-179">IID</span></span><br/>                      | <span data-ttu-id="be3c2-180">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="be3c2-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

