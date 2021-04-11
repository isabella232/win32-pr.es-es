---
description: Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo. La colección de instantáneas, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Método ExportSnapshot de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276183"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="79724-104">Método ExportSnapshot de la \_ clase CollectionSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="79724-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="79724-105">Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo.</span><span class="sxs-lookup"><span data-stu-id="79724-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="79724-106">La colección de instantáneas, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.</span><span class="sxs-lookup"><span data-stu-id="79724-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="79724-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79724-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="79724-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79724-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79724-109">*SnapshotCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79724-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79724-110">Referencia a una [**\_ colección CIM**](cim-collection.md) que representa la colección de instantáneas que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="79724-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="79724-111">*ExportDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79724-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79724-112">Ruta de acceso completa del directorio al que se va a exportar la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="79724-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="79724-113">Si la propiedad **CreateVmExportSubdirectory** del parámetro *ExportSettingData* se establece en **true** , este directorio se puede reutilizar para exportar varias colecciones de sistemas virtuales y este método coloca cada definición de colección de sistemas virtuales en un subdirectorio independiente en esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="79724-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="79724-114">*ExportSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79724-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79724-115">Instancia de [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) que representa la configuración de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="79724-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="79724-116">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79724-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79724-117">Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="79724-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="79724-118">Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="79724-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79724-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79724-119">Return value</span></span>

<span data-ttu-id="79724-120">Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="79724-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="79724-121">Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del trabajo se puede usar para realizar el seguimiento del progreso de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="79724-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="79724-122">Cualquier otro valor devuelto indica un error.</span><span class="sxs-lookup"><span data-stu-id="79724-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="79724-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79724-123">Requirements</span></span>



| <span data-ttu-id="79724-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79724-124">Requirement</span></span> | <span data-ttu-id="79724-125">Value</span><span class="sxs-lookup"><span data-stu-id="79724-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79724-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79724-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79724-127">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="79724-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="79724-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79724-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79724-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="79724-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="79724-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79724-130">Namespace</span></span><br/>                | <span data-ttu-id="79724-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="79724-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79724-132">MOF</span><span class="sxs-lookup"><span data-stu-id="79724-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79724-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79724-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79724-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79724-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79724-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79724-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79724-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="79724-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79724-137">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="79724-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




