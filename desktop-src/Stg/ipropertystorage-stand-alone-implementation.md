---
title: 'IPropertyStorage: implementación independiente'
description: La implementación independiente proporcionada por el sistema de IPropertySetStorage incluye una implementación de IPropertyStorage, la interfaz que lee y escribe propiedades en un almacenamiento de conjunto de propiedades.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- 'IPropertyStorage: implementación independiente'
- IPropertyStorage Strctd STG, implementaciones, independiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420883"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="0d590-105">IPropertyStorage: implementación independiente</span><span class="sxs-lookup"><span data-stu-id="0d590-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="0d590-106">La implementación independiente proporcionada por el sistema de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) incluye una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), la interfaz que lee y escribe propiedades en un almacenamiento de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d590-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="0d590-107">La interfaz **IPropertySetStorage** crea y abre conjuntos de propiedades en un almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="0d590-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="0d590-108">Las interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) y [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) también se proporcionan en la implementación independiente.</span><span class="sxs-lookup"><span data-stu-id="0d590-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="0d590-109">Para obtener un puntero a la implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), llame a la función [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para crear un nuevo conjunto de propiedades o [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obtener el puntero de interfaz en un conjunto de propiedades existente (o llame a los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de la implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).</span><span class="sxs-lookup"><span data-stu-id="0d590-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="0d590-110">La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crea conjuntos de propiedades en cualquier almacenamiento o objeto de flujo, no solo en flujos y almacenamientos de archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="0d590-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="0d590-111">La implementación independiente no depende de archivos compuestos y se puede usar con cualquier implementación de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="0d590-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="0d590-112">Para obtener más información sobre la implementación de archivos compuestos de esta interfaz, vea [IPropertyStorage-composición de archivos compuestos](ipropertystorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="0d590-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0d590-113">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="0d590-113">When to Use</span></span>

<span data-ttu-id="0d590-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para administrar propiedades dentro de un único conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d590-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="0d590-115">Sus métodos permiten leer, escribir y eliminar ambas propiedades y los nombres de cadena opcionales que se pueden asociar a los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d590-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="0d590-116">Otros métodos admiten las operaciones de almacenamiento estándar commit y Revert.</span><span class="sxs-lookup"><span data-stu-id="0d590-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="0d590-117">También hay un método que establece las horas asociadas al almacenamiento de propiedades y otro que permite usar la asignación de un CLSID para asociar otro código, como el código de la interfaz de usuario, con la propiedad establecida.</span><span class="sxs-lookup"><span data-stu-id="0d590-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="0d590-118">El método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) proporciona un puntero a la implementación independiente de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que enumera las propiedades del conjunto.</span><span class="sxs-lookup"><span data-stu-id="0d590-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="0d590-119">Formatos de conjunto de propiedades de las versiones 0 y 1</span><span class="sxs-lookup"><span data-stu-id="0d590-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="0d590-120">La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los formatos de serialización de la versión 0 y la versión 1.</span><span class="sxs-lookup"><span data-stu-id="0d590-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="0d590-121">Para obtener más información, vea [serialización de conjuntos de propiedades](version-0-vs--version-1-property-set-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="0d590-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="0d590-122">Los conjuntos de propiedades se crean en el formato de la versión 0 y permanecen en ese formato a menos que se soliciten nuevas características.</span><span class="sxs-lookup"><span data-stu-id="0d590-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="0d590-123">En ese momento, el formato se actualiza a la versión 1.</span><span class="sxs-lookup"><span data-stu-id="0d590-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="0d590-124">Por ejemplo, si se crea un conjunto de propiedades con la \_ marca predeterminada PROPSETFLAG, su formato es la versión 0.</span><span class="sxs-lookup"><span data-stu-id="0d590-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="0d590-125">Siempre que los tipos de propiedad que se ajustan al formato de la versión 0 se escriben y se leen de ese conjunto de propiedades, el conjunto de propiedades permanece en formato de la versión 0.</span><span class="sxs-lookup"><span data-stu-id="0d590-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="0d590-126">Si un tipo de propiedad de la versión 1 se escribe en el conjunto de propiedades, el conjunto de propiedades se actualiza automáticamente a la versión 1.</span><span class="sxs-lookup"><span data-stu-id="0d590-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="0d590-127">Posteriormente, las implementaciones que solo entienden la versión 0 ya no podrán leer ese conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d590-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="0d590-128">Tipos IPropertyStorage y Variant</span><span class="sxs-lookup"><span data-stu-id="0d590-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="0d590-129">La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no admite los tipos Variant VT \_ Unknown o VT \_ Dispatch en el miembro **VT** de la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="0d590-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="0d590-130">Se admiten los siguientes tipos de variante dentro de SafeArray; es decir, estos valores se pueden combinar con \_ la matriz VT en el miembro **VT** de la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="0d590-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="0d590-131">Tipos de variante admitidos en SafeArray por implementación de archivo compuesto de [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="0d590-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="0d590-132">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="0d590-132">VT\_I1</span></span>

<span data-ttu-id="0d590-133">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="0d590-133">VT\_UI1</span></span>

<span data-ttu-id="0d590-134">I2 de VT \_</span><span class="sxs-lookup"><span data-stu-id="0d590-134">VT\_I2</span></span>

<span data-ttu-id="0d590-135">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="0d590-135">VT\_UI2</span></span>

<span data-ttu-id="0d590-136">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0d590-136">VT\_I4</span></span>

<span data-ttu-id="0d590-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="0d590-137">VT\_UI4</span></span>

<span data-ttu-id="0d590-138">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="0d590-138">VT\_INT</span></span>

<span data-ttu-id="0d590-139">VT \_ uint</span><span class="sxs-lookup"><span data-stu-id="0d590-139">VT\_UINT</span></span>

<span data-ttu-id="0d590-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="0d590-140">VT\_R4</span></span>

<span data-ttu-id="0d590-141">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="0d590-141">VT\_R8</span></span>

<span data-ttu-id="0d590-142">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="0d590-142">VT\_CY</span></span>

<span data-ttu-id="0d590-143">fecha de VT \_</span><span class="sxs-lookup"><span data-stu-id="0d590-143">VT\_DATE</span></span>

<span data-ttu-id="0d590-144">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="0d590-144">VT\_BSTR</span></span>

<span data-ttu-id="0d590-145">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="0d590-145">VT\_BOOL</span></span>

<span data-ttu-id="0d590-146">VT \_ decimal</span><span class="sxs-lookup"><span data-stu-id="0d590-146">VT\_DECIMAL</span></span>

<span data-ttu-id="0d590-147">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="0d590-147">VT\_ERROR</span></span>

<span data-ttu-id="0d590-148">VT ( \_ variante)</span><span class="sxs-lookup"><span data-stu-id="0d590-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="0d590-149">Cuando \_ se combina VT Variant con una \_ matriz de VT, el propio SafeArray contiene estructuras [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="0d590-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="0d590-150">Sin embargo, los tipos de estos elementos se deben tomar de la lista anterior, no pueden ser de \_ tipo VT y no pueden incluir los indicadores de VT \_ , \_ matriz VT o VT \_ BYREF.</span><span class="sxs-lookup"><span data-stu-id="0d590-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="0d590-151">Métodos IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="0d590-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="0d590-152">La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="0d590-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="0d590-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="0d590-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-154">Lee las propiedades especificadas en la matriz *rgpspec* y proporciona los valores de todas las propiedades válidas en la matriz *Rgvar* de elementos [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="0d590-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="0d590-155">En la implementación independiente y proporcionada por el sistema, los identificadores de propiedad duplicados que hacen referencia a los tipos de almacenamiento o de secuencia producen varias llamadas a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) y el éxito o el error de [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depende de la capacidad de la implementación de almacenamiento subyacente para compartir almacenamientos abiertos.</span><span class="sxs-lookup"><span data-stu-id="0d590-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="0d590-156">Además, para asegurarse de que la operación segura para subprocesos se solicita varias veces a través del mismo puntero [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , el objeto abierto se realizará correctamente o producirá un error en función de si la propiedad ya está abierta o no, y de si el sistema de archivos subyacente controla varias aperturas de una secuencia o almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="0d590-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="0d590-157">Por lo tanto, la operación [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) en una propiedad de flujo o de valor de almacenamiento siempre da como resultado una llamada a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), pasando el acceso (STGM \_ ReadWrite, por ejemplo) y los valores compartidos (STGM \_ recurso compartido \_ exclusivo, por ejemplo) especificados cuando el conjunto de propiedades se abrió o creó originalmente.</span><span class="sxs-lookup"><span data-stu-id="0d590-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="0d590-158">Si se produce un error en el método, los valores escritos en *rgvar* no \[ \] están definidos.</span><span class="sxs-lookup"><span data-stu-id="0d590-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="0d590-159">Si algunas propiedades de flujo o de valor de almacenamiento se abren correctamente pero se produce un error antes de que se complete la ejecución, estas propiedades deben liberarse antes de que el método vuelva.</span><span class="sxs-lookup"><span data-stu-id="0d590-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="0d590-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-161">Escribe las propiedades especificadas en la matriz *rgpspec* \[ \] , asignándoles las etiquetas y los valores de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificados en *rgvar* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="0d590-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="0d590-162">A las propiedades que ya existen se les asignan los valores de **PROPVARIANT** especificados y se crean las propiedades que no existen actualmente.</span><span class="sxs-lookup"><span data-stu-id="0d590-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="0d590-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-164">Elimina las propiedades especificadas en *rgpspec* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="0d590-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="0d590-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="0d590-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-166">Lee los nombres de cadena existentes asociados a los identificadores de propiedad especificados en la matriz *rgpropid* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="0d590-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="0d590-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-168">Asigna nombres de cadena especificados en la matriz *rglpwstrName* a los identificadores de propiedad especificados en la matriz *rgpropid* .</span><span class="sxs-lookup"><span data-stu-id="0d590-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="0d590-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-170">Elimina los nombres de cadena de los identificadores de propiedad especificados en la matriz *rgpropid* escribiendo **null** en el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d590-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="0d590-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-172">Establece el **CLSID** de la secuencia del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d590-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="0d590-173">En la implementación independiente, al establecer el CLSID en un conjunto de propiedades no simples (uno que puede contener propiedades de almacenamiento o con valores de flujo, tal como se describe en [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) también se establece el CLSID en el subalmacenamiento subyacente para que se pueda obtener a través de una llamada a [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span><span class="sxs-lookup"><span data-stu-id="0d590-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="0d590-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="0d590-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-175">En el caso de conjuntos de propiedades simples y no simples, vacía la imagen de memoria en el subsistema de disco.</span><span class="sxs-lookup"><span data-stu-id="0d590-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="0d590-176">Además, en el caso de conjuntos de propiedades de modo de transacción no simples, este método llama a [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) en el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d590-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="0d590-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-178">Solo para conjuntos de propiedades no simples, llama al método [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) del almacenamiento subyacente y vuelve a abrir la secuencia ' contents '.</span><span class="sxs-lookup"><span data-stu-id="0d590-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="0d590-179">En el caso de los conjuntos de propiedades simples, solo devuelve E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d590-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="0d590-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-181">Crea un objeto enumerador que implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), los métodos de los que se puede llamar para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que proporcionan información sobre cada una de las propiedades del conjunto.</span><span class="sxs-lookup"><span data-stu-id="0d590-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="0d590-182">Esta implementación crea una matriz en la que se lee todo el conjunto de propiedades y que se puede compartir cuando se llama a [**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) .</span><span class="sxs-lookup"><span data-stu-id="0d590-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="0d590-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-184">Rellena los miembros de una estructura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , que contiene información sobre el conjunto de propiedades como un todo.</span><span class="sxs-lookup"><span data-stu-id="0d590-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="0d590-185">En la devolución, proporciona un puntero a la estructura.</span><span class="sxs-lookup"><span data-stu-id="0d590-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="0d590-186">En el caso de los conjuntos de almacenamiento no simples, esta implementación llama a [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) para obtener la información de la secuencia o el almacenamiento subyacente.</span><span class="sxs-lookup"><span data-stu-id="0d590-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="0d590-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="0d590-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="0d590-188">Solo para conjuntos de propiedades no simples, establece las horas admitidas por el almacenamiento subyacente.</span><span class="sxs-lookup"><span data-stu-id="0d590-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="0d590-189">Esta implementación de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) llama al método [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) del almacenamiento subyacente para modificar las horas.</span><span class="sxs-lookup"><span data-stu-id="0d590-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="0d590-190">Admite las horas admitidas por el método subyacente, que puede ser la hora de modificación, el tiempo de acceso o la hora de creación.</span><span class="sxs-lookup"><span data-stu-id="0d590-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="0d590-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d590-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d590-192">IPropertySetStorage: implementación independiente</span><span class="sxs-lookup"><span data-stu-id="0d590-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="0d590-193">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="0d590-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="0d590-194">**IStorage:: SetElementTimes**</span><span class="sxs-lookup"><span data-stu-id="0d590-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="0d590-195">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="0d590-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="0d590-196">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="0d590-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="0d590-197">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="0d590-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 