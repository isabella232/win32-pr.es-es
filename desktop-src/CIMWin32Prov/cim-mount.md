---
description: La \_ clase de montaje CIM representa una asociación entre un sistema de archivos y un directorio al que está asociado.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153227"
---
# <a name="cim_mount-class"></a><span data-ttu-id="eaeed-103">\_Clase de montaje CIM</span><span class="sxs-lookup"><span data-stu-id="eaeed-103">CIM\_Mount class</span></span>

<span data-ttu-id="eaeed-104">La clase de **\_ montaje CIM** representa una asociación entre un sistema de archivos y un directorio al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="eaeed-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="eaeed-105">La semántica de esta relación requiere que el directorio montado esté contenido en un sistema de archivos (a través de la Asociación de almacenamiento de archivos) que sea diferente del sistema de archivos al que se hace referencia como dependiente.</span><span class="sxs-lookup"><span data-stu-id="eaeed-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="eaeed-106">El sistema de archivos que contiene el directorio puede ser local o remoto.</span><span class="sxs-lookup"><span data-stu-id="eaeed-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="eaeed-107">Por ejemplo, un sistema de archivos local en un equipo de Solaris puede montar un directorio del sistema de archivos al que se tiene acceso a través de la unidad CDROM del equipo (es decir, otro sistema de archivos local).</span><span class="sxs-lookup"><span data-stu-id="eaeed-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="eaeed-108">Por otro lado, en un caso "remoto", el directorio se exporta primero por su sistema de archivos, que se hospeda en otro equipo que actúa, por ejemplo, como un servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="eaeed-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="eaeed-109">Para distinguir los dos montajes, una asociación de [**\_ exportación de CIM**](cim-export.md) siempre debe definirse para los directorios de acceso remoto o montados.</span><span class="sxs-lookup"><span data-stu-id="eaeed-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eaeed-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="eaeed-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eaeed-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eaeed-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eaeed-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eaeed-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eaeed-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="eaeed-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaeed-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eaeed-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="eaeed-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="eaeed-115">Members</span></span>

<span data-ttu-id="eaeed-116">La clase de **\_ montaje CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eaeed-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="eaeed-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eaeed-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eaeed-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eaeed-118">Properties</span></span>

<span data-ttu-id="eaeed-119">La clase de **\_ montaje CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eaeed-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eaeed-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="eaeed-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaeed-121">Tipo de datos **: \_ directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="eaeed-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="eaeed-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eaeed-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaeed-123">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="eaeed-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="eaeed-124">Un [**\_ directorio CIM**](cim-directory.md) que describe el directorio montado.</span><span class="sxs-lookup"><span data-stu-id="eaeed-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="eaeed-125">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="eaeed-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaeed-126">Tipo de datos: **CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="eaeed-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="eaeed-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eaeed-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaeed-128">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="eaeed-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="eaeed-129">Una [**\_ NFS de CIM**](cim-nfs.md) que describe el sistema de archivos en el que se monta el directorio.</span><span class="sxs-lookup"><span data-stu-id="eaeed-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaeed-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eaeed-130">Remarks</span></span>

<span data-ttu-id="eaeed-131">**CIM \_ El montaje** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="eaeed-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="eaeed-132">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="eaeed-132">WMI does not implement this class.</span></span>

<span data-ttu-id="eaeed-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="eaeed-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eaeed-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="eaeed-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaeed-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaeed-135">Requirements</span></span>



| <span data-ttu-id="eaeed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaeed-136">Requirement</span></span> | <span data-ttu-id="eaeed-137">Value</span><span class="sxs-lookup"><span data-stu-id="eaeed-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaeed-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaeed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="eaeed-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eaeed-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eaeed-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaeed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="eaeed-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaeed-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaeed-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eaeed-142">Namespace</span></span><br/>                | <span data-ttu-id="eaeed-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eaeed-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eaeed-144">MOF</span><span class="sxs-lookup"><span data-stu-id="eaeed-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaeed-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaeed-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaeed-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eaeed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaeed-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaeed-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaeed-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="eaeed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaeed-149">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="eaeed-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

