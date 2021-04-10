---
description: La \_ clase CIM SupportAccess define cómo obtener ayuda para un producto.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: CIM_SupportAccess (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153123"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="6a344-103">\_Clase SupportAccess de CIM</span><span class="sxs-lookup"><span data-stu-id="6a344-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="6a344-104">La clase **CIM \_ SupportAccess** define cómo obtener ayuda para un producto.</span><span class="sxs-lookup"><span data-stu-id="6a344-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a344-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6a344-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6a344-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6a344-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6a344-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6a344-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6a344-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6a344-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a344-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a344-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="6a344-110">Members</span><span class="sxs-lookup"><span data-stu-id="6a344-110">Members</span></span>

<span data-ttu-id="6a344-111">La clase **CIM \_ SupportAccess** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6a344-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="6a344-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a344-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a344-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a344-113">Properties</span></span>

<span data-ttu-id="6a344-114">La clase **CIM \_ SupportAccess** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a344-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a344-115">**CommunicationInfo**</span><span class="sxs-lookup"><span data-stu-id="6a344-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a344-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a344-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a344-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a344-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a344-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU \| de DMTF 002,11 "," MIF. \|FRU 002,12 de DMTF \| ")</span><span class="sxs-lookup"><span data-stu-id="6a344-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="6a344-119">Detalles del modo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="6a344-119">Details of the communication mode.</span></span> <span data-ttu-id="6a344-120">Por ejemplo, si la propiedad **CommunicationMode** es "Phone", esta propiedad especifica el número de teléfono al que llamar.</span><span class="sxs-lookup"><span data-stu-id="6a344-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="6a344-121">**CommunicationMode**</span><span class="sxs-lookup"><span data-stu-id="6a344-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a344-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a344-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a344-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a344-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a344-124">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Compatibilidad con DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="6a344-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6a344-125">Forma de comunicación que se va a usar para obtener soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="6a344-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a344-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a344-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="6a344-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Teléfono** (2)</span><span class="sxs-lookup"><span data-stu-id="6a344-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="6a344-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span><span class="sxs-lookup"><span data-stu-id="6a344-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="6a344-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span><span class="sxs-lookup"><span data-stu-id="6a344-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="6a344-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Servicio en línea** (5)</span><span class="sxs-lookup"><span data-stu-id="6a344-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="6a344-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Página Web** (6)</span><span class="sxs-lookup"><span data-stu-id="6a344-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6a344-132">Página web</span><span class="sxs-lookup"><span data-stu-id="6a344-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="6a344-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span><span class="sxs-lookup"><span data-stu-id="6a344-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="6a344-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Correo electrónico** (8)</span><span class="sxs-lookup"><span data-stu-id="6a344-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6a344-135">Email</span><span class="sxs-lookup"><span data-stu-id="6a344-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a344-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a344-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a344-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a344-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a344-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a344-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a344-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Compatibilidad con DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="6a344-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6a344-140">Descripción textual del tipo de soporte proporcionado.</span><span class="sxs-lookup"><span data-stu-id="6a344-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="6a344-141">**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="6a344-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a344-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a344-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a344-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a344-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a344-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Compatibilidad con DMTF \| 001,2 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6a344-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6a344-145">Región geográfica o dialecto de lenguaje al que pertenece este recurso de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="6a344-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="6a344-146">**SupportAccessId**</span><span class="sxs-lookup"><span data-stu-id="6a344-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a344-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a344-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a344-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a344-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a344-149">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6a344-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6a344-150">Cadena de forma libre arbitraria definida por el proveedor del producto o por la organización que implementa el producto.</span><span class="sxs-lookup"><span data-stu-id="6a344-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="6a344-151">Esta propiedad, ya que es una clave, debe ser única en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="6a344-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a344-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a344-152">Remarks</span></span>

<span data-ttu-id="6a344-153">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6a344-153">WMI does not implement this class.</span></span>

<span data-ttu-id="6a344-154">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6a344-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6a344-155">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6a344-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a344-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a344-156">Requirements</span></span>



| <span data-ttu-id="6a344-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a344-157">Requirement</span></span> | <span data-ttu-id="6a344-158">Value</span><span class="sxs-lookup"><span data-stu-id="6a344-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a344-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a344-159">Minimum supported client</span></span><br/> | <span data-ttu-id="6a344-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a344-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a344-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a344-161">Minimum supported server</span></span><br/> | <span data-ttu-id="6a344-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a344-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a344-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a344-163">Namespace</span></span><br/>                | <span data-ttu-id="6a344-164">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6a344-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a344-165">MOF</span><span class="sxs-lookup"><span data-stu-id="6a344-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a344-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a344-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a344-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a344-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a344-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a344-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

