---
title: MDM_Policy_Result01_TextInput02 (clase)
description: La \_ clase Result01 de la Directiva MDM \_ \_ TextInput02 representa las directivas de entrada de texto disponibles.
ms.assetid: d0ab2d69-6d43-410e-936a-cb87a521d5f3
keywords:
- MDM_Policy_Result01_TextInput02 (clase)
- MDM_Policy_Result01_TextInput02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02.InstanceID
- MDM_Policy_Result01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a0c02c2afe70f3e7122de0c3d888c42ac179317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490156"
---
# <a name="mdm_policy_result01_textinput02-class"></a><span data-ttu-id="c886b-105">\_ \_ Clase TextInput02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="c886b-105">MDM\_Policy\_Result01\_TextInput02 class</span></span>

<span data-ttu-id="c886b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c886b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c886b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c886b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c886b-108">La clase Result01 de la **\_ Directiva MDM \_ \_ TextInput02** representa las directivas de entrada de texto disponibles.</span><span class="sxs-lookup"><span data-stu-id="c886b-108">The **MDM\_Policy\_Result01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="c886b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c886b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c886b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c886b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_TextInput02
{
  string InstanceID;
  string ParentID;
  sint32 AllowIMENetworkAccess;
  sint32 AllowIMELogging;
  sint32 AllowJapaneseNonPublishingStandardGlyph;
  sint32 AllowJapaneseIVSCharacters;
  sint32 AllowJapaneseUserDictionary;
  sint32 AllowKeyboardTextSuggestions;
  sint32 AllowJapaneseIMESurrogatePairCharacters;
  sint32 ExcludeJapaneseIMEExceptShiftJIS;
  sint32 ExcludeJapaneseIMEExceptJIS0208;
  sint32 ExcludeJapaneseIMEExceptJIS0208andEUDC;
  sint32 AllowLanguageFeaturesUninstall;
  sint32 AllowInputPanel;
};
```

## <a name="members"></a><span data-ttu-id="c886b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c886b-111">Members</span></span>

<span data-ttu-id="c886b-112">La clase Result01 de la **\_ Directiva MDM \_ \_ TextInput02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c886b-112">The **MDM\_Policy\_Result01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="c886b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c886b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c886b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c886b-114">Properties</span></span>

<span data-ttu-id="c886b-115">La **clase \_ \_ Result01 de \_ TextInput02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c886b-115">The **MDM\_Policy\_Result01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c886b-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="c886b-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c886b-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="c886b-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="c886b-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="c886b-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-131">AllowJapaneseNonPublishingStandardGlyph</span><span class="sxs-lookup"><span data-stu-id="c886b-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="c886b-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="c886b-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="c886b-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-143">ExcludeJapaneseIMEExceptJIS0208</span><span class="sxs-lookup"><span data-stu-id="c886b-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span><span class="sxs-lookup"><span data-stu-id="c886b-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c886b-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="c886b-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c886b-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c886b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c886b-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c886b-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c886b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c886b-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886b-155">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c886b-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c886b-156">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c886b-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="c886b-157">Para esta clase, la cadena es "TextInput"</span><span class="sxs-lookup"><span data-stu-id="c886b-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="c886b-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c886b-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886b-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c886b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886b-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c886b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886b-161">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c886b-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c886b-162">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c886b-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="c886b-163">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="c886b-163">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c886b-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c886b-164">Requirements</span></span>



| <span data-ttu-id="c886b-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c886b-165">Requirement</span></span> | <span data-ttu-id="c886b-166">Value</span><span class="sxs-lookup"><span data-stu-id="c886b-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c886b-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c886b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c886b-168">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c886b-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c886b-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c886b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c886b-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c886b-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c886b-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c886b-171">Namespace</span></span><br/>                | <span data-ttu-id="c886b-172">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="c886b-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c886b-173">MOF</span><span class="sxs-lookup"><span data-stu-id="c886b-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c886b-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c886b-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c886b-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c886b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c886b-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c886b-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c886b-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="c886b-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c886b-178">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="c886b-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

