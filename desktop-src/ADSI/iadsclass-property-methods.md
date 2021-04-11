---
title: Métodos de la propiedad IADsClass (iAds. h)
description: Los métodos de propiedad de la interfaz IADsClass obtienen o establecen las siguientes propiedades. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsClass ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150777"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="4f904-105">Métodos de propiedad IADsClass</span><span class="sxs-lookup"><span data-stu-id="4f904-105">IADsClass Property Methods</span></span>

<span data-ttu-id="4f904-106">Los métodos de propiedad de la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) obtienen o establecen las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="4f904-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="4f904-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4f904-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4f904-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f904-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4f904-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f904-109">**Abstract**</span></span>
<span data-ttu-id="4f904-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-111">Valor booleano que indica si esta clase es abstracta o no abstracta.</span><span class="sxs-lookup"><span data-stu-id="4f904-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="4f904-112">Si es **true**, esta clase es una clase abstracta y no se puede crear directamente una instancia de ella en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="4f904-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="4f904-113">Las clases abstractas solo se pueden usar como superclases.</span><span class="sxs-lookup"><span data-stu-id="4f904-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="4f904-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-115">Tipo de datos de scripting: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f904-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-116">**AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="4f904-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="4f904-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-118">Matriz de cadenas ADsPath que indican las clases de Super auxiliar de las que se deriva esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="4f904-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-120">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-121">**Auxiliar**</span><span class="sxs-lookup"><span data-stu-id="4f904-121">**Auxiliary**</span></span>
<span data-ttu-id="4f904-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-123">Valor booleano que indica si esta clase es auxiliar o no.</span><span class="sxs-lookup"><span data-stu-id="4f904-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="4f904-124">Si es **true**, esta clase es una clase auxiliar y no se pueden crear instancias directamente en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="4f904-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="4f904-125">Las clases auxiliares solo se pueden usar como súper clases de otras clases auxiliares o como origen de propiedades adicionales en clases estructurales.</span><span class="sxs-lookup"><span data-stu-id="4f904-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="4f904-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-127">Tipo de datos de scripting: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f904-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-128">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="4f904-128">**CLSID**</span></span>
<span data-ttu-id="4f904-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-130">CLSID opcional específico del proveedor que identifica el objeto COM que implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="4f904-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-132">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f904-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-133">**Contenedor**</span><span class="sxs-lookup"><span data-stu-id="4f904-133">**Container**</span></span>
<span data-ttu-id="4f904-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-135">Valor booleano que indica si esta clase puede ser un contenedor de otras clases de objeto.</span><span class="sxs-lookup"><span data-stu-id="4f904-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="4f904-136">Si este valor es **true**, puede llamar al método **Get \_ Container** para obtener una matriz de las clases de objeto que esta clase puede contener.</span><span class="sxs-lookup"><span data-stu-id="4f904-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="4f904-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-138">Tipo de datos de scripting: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f904-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-139">**Containment**</span><span class="sxs-lookup"><span data-stu-id="4f904-139">**Containment**</span></span>
<span data-ttu-id="4f904-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-141">Matriz **BSTR** en la que cada elemento es el nombre de una clase de objeto que esta clase puede contener.</span><span class="sxs-lookup"><span data-stu-id="4f904-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="4f904-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-143">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-144">**DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="4f904-144">**DerivedFrom**</span></span>
<span data-ttu-id="4f904-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-146">Matriz de cadenas ADsPath que indican las clases de las que se deriva esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="4f904-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-148">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-149">**HelpFileContext**</span><span class="sxs-lookup"><span data-stu-id="4f904-149">**HelpFileContext**</span></span>
<span data-ttu-id="4f904-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-151">IDENTIFICADOR de contexto dentro de **HelpFileName** donde se puede encontrar información específica de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="4f904-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-153">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="4f904-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-154">**HelpFileName**</span><span class="sxs-lookup"><span data-stu-id="4f904-154">**HelpFileName**</span></span>
<span data-ttu-id="4f904-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-156">Nombre de un archivo de ayuda que contiene más información sobre los objetos de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="4f904-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-158">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f904-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-159">**MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="4f904-159">**MandatoryProperties**</span></span>
<span data-ttu-id="4f904-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-161">**SAFEARRAY** de **Variant** s que enumera las propiedades que se deben establecer para que esta clase se escriba en el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4f904-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="4f904-162">Si la clase solo contiene una propiedad, **Get \_ MandatoryProperties** devolverá un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="4f904-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="4f904-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-164">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-165">**NamingProperties**</span><span class="sxs-lookup"><span data-stu-id="4f904-165">**NamingProperties**</span></span>
<span data-ttu-id="4f904-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-167">**SAFEARRAY** de **BSTR** s que enumera las propiedades utilizadas para asignar nombres a los atributos de esta clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="4f904-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="4f904-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-169">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-170">**OID**</span><span class="sxs-lookup"><span data-stu-id="4f904-170">**OID**</span></span>
<span data-ttu-id="4f904-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-172">Identificador de objeto específico del proveedor que define esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="4f904-173">Esto se proporciona para permitir la extensión de esquema, mediante Active Directory, en servicios de directorio que requieran OID específicos del proveedor para las clases.</span><span class="sxs-lookup"><span data-stu-id="4f904-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="4f904-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-175">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f904-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-176">**OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="4f904-176">**OptionalProperties**</span></span>
<span data-ttu-id="4f904-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-178">**SAFEARRAY** de **Variant** s que enumera las propiedades opcionales para esta clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="4f904-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="4f904-179">Si la clase solo contiene una propiedad, **Get \_ OptionalProperties** devolverá un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="4f904-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="4f904-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-181">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-182">**PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="4f904-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="4f904-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-184">Matriz de cadenas ADsPath que indican las clases de esquema que pueden contener instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f904-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="4f904-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4f904-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f904-186">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="4f904-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f904-187">**PrimaryInterface**</span><span class="sxs-lookup"><span data-stu-id="4f904-187">**PrimaryInterface**</span></span>
<span data-ttu-id="4f904-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f904-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f904-189">GUID opcional del identificador específico del proveedor que asocia una interfaz a los objetos de esta clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="4f904-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="4f904-190">Por ejemplo, la clase "User" que admite [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) y **PrimaryInterface** se identifica mediante **IID \_ IADsUser**.</span><span class="sxs-lookup"><span data-stu-id="4f904-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="4f904-191">Debe estar en el formato de cadena estándar de un GUID, tal y como se define en COM.</span><span class="sxs-lookup"><span data-stu-id="4f904-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="4f904-192">Este GUID es el valor que aparece en la propiedad [**IADs:: get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) en las instancias de esta clase para los proveedores que implementan esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f904-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="4f904-193">La identificación de una clase de esquema por parte de IID de la interfaz principal del código de clase permite el uso de **QueryInterface** en tiempo de ejecución para determinar si un objeto es de la clase deseada.</span><span class="sxs-lookup"><span data-stu-id="4f904-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="4f904-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f904-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f904-195">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f904-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4f904-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4f904-196">Examples</span></span>

<span data-ttu-id="4f904-197">En el ejemplo de código siguiente se muestra cómo utilizar la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar si un objeto puede ser un contenedor y, si es así, enumera los nombres de los objetos contenidos.</span><span class="sxs-lookup"><span data-stu-id="4f904-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="4f904-198">En el ejemplo de código siguiente se muestra cómo utilizar la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar si un objeto puede ser un contenedor y, si es así, enumera los nombres de los objetos contenidos.</span><span class="sxs-lookup"><span data-stu-id="4f904-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="4f904-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f904-199">Requirements</span></span>



| <span data-ttu-id="4f904-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f904-200">Requirement</span></span> | <span data-ttu-id="4f904-201">Value</span><span class="sxs-lookup"><span data-stu-id="4f904-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f904-202">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f904-202">Minimum supported client</span></span><br/> | <span data-ttu-id="4f904-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f904-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f904-204">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f904-204">Minimum supported server</span></span><br/> | <span data-ttu-id="4f904-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f904-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f904-206">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f904-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f904-207"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f904-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4f904-208">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f904-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f904-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f904-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f904-210">IID</span><span class="sxs-lookup"><span data-stu-id="4f904-210">IID</span></span><br/>                      | <span data-ttu-id="4f904-211">IID \_ IADsClass se define como C8F93DD0-4AE0-11cf-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="4f904-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4f904-212">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f904-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f904-213">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="4f904-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="4f904-214">**IADsClass:: Qualifiers**</span><span class="sxs-lookup"><span data-stu-id="4f904-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





