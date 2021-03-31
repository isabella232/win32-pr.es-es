---
title: Win32_RDSHCollection (clase)
description: Administra una colección de hosts de sesión Escritorio remoto.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDSHCollection de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490972"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="c512e-105">\_Clase Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="c512e-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="c512e-106">Administra una colección de hosts de sesión Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c512e-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="c512e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c512e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c512e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c512e-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="c512e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c512e-109">Members</span></span>

<span data-ttu-id="c512e-110">La **clase \_ RDSHCollection de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c512e-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="c512e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c512e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c512e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c512e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c512e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c512e-113">Methods</span></span>

<span data-ttu-id="c512e-114">La clase **Win32 \_ RDSHCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c512e-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="c512e-115">Método</span><span class="sxs-lookup"><span data-stu-id="c512e-115">Method</span></span>                                                                      | <span data-ttu-id="c512e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c512e-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c512e-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="c512e-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="c512e-118">Recupera un valor de propiedad de entero de un **objeto \_ RDSHCollection de Win32** .</span><span class="sxs-lookup"><span data-stu-id="c512e-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="c512e-119">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="c512e-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="c512e-120">Recupera un valor de propiedad de cadena de un objeto **\_ RDSHCollection de Win32** .</span><span class="sxs-lookup"><span data-stu-id="c512e-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="c512e-121">**KeyValueCompareAndSet**</span><span class="sxs-lookup"><span data-stu-id="c512e-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="c512e-122">Compara la clave especificada de la colección con un comparand; Si coinciden, la clave se establece en un valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="c512e-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="c512e-123">Si la clave no existe, el método insertará la clave en la colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="c512e-124">**KeyValueDelete**</span><span class="sxs-lookup"><span data-stu-id="c512e-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="c512e-125">Elimina la clave especificada (y el valor asociado) de la colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="c512e-126">**KeyValueGet**</span><span class="sxs-lookup"><span data-stu-id="c512e-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="c512e-127">Recupera el valor asociado a la clave especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="c512e-128">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="c512e-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="c512e-129">Actualiza un valor de propiedad de entero de un objeto **\_ RDSHCollection de Win32** .</span><span class="sxs-lookup"><span data-stu-id="c512e-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="c512e-130">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="c512e-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="c512e-131">Actualiza un valor de propiedad de cadena de un objeto **\_ RDSHCollection de Win32** .</span><span class="sxs-lookup"><span data-stu-id="c512e-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="c512e-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c512e-132">Properties</span></span>

<span data-ttu-id="c512e-133">La **clase \_ RDSHCollection de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c512e-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c512e-134">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c512e-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c512e-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c512e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c512e-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c512e-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c512e-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c512e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c512e-138">Obtiene y establece el alias de la colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c512e-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c512e-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c512e-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c512e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c512e-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c512e-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c512e-142">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c512e-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c512e-143">Obtiene y establece la descripción de la colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c512e-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c512e-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c512e-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c512e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c512e-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c512e-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c512e-147">Obtiene y establece el nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c512e-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c512e-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c512e-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c512e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c512e-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c512e-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c512e-151">**Windows server 2012 R2 y Windows server 2012:** Esta propiedad no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c512e-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="c512e-152">Tipo de colección.</span><span class="sxs-lookup"><span data-stu-id="c512e-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="c512e-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Normal** (0)</span><span class="sxs-lookup"><span data-stu-id="c512e-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c512e-154">(2)</span><span class="sxs-lookup"><span data-stu-id="c512e-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="c512e-155">Reservado</span><span class="sxs-lookup"><span data-stu-id="c512e-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="c512e-156">(3)</span><span class="sxs-lookup"><span data-stu-id="c512e-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c512e-157">Reservado</span><span class="sxs-lookup"><span data-stu-id="c512e-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="c512e-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span><span class="sxs-lookup"><span data-stu-id="c512e-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="c512e-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonal** (5)</span><span class="sxs-lookup"><span data-stu-id="c512e-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="c512e-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c512e-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c512e-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c512e-161">Requirements</span></span>



| <span data-ttu-id="c512e-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="c512e-162">Requirement</span></span> | <span data-ttu-id="c512e-163">Value</span><span class="sxs-lookup"><span data-stu-id="c512e-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c512e-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c512e-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c512e-165">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c512e-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c512e-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c512e-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c512e-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c512e-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c512e-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c512e-168">Namespace</span></span><br/>                | <span data-ttu-id="c512e-169">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="c512e-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c512e-170">MOF</span><span class="sxs-lookup"><span data-stu-id="c512e-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c512e-171"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c512e-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c512e-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c512e-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c512e-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c512e-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c512e-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="c512e-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c512e-175">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c512e-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

