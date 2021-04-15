---
description: Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Método ExportReferencePoint de la clase Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688717"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="13fe1-104">Método ExportReferencePoint de la \_ clase CollectionReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="13fe1-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="13fe1-105">Exporta una colección de puntos de referencia a un archivo.</span><span class="sxs-lookup"><span data-stu-id="13fe1-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="13fe1-106">La colección de puntos de referencia, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.</span><span class="sxs-lookup"><span data-stu-id="13fe1-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fe1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13fe1-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="13fe1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13fe1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13fe1-109">*ReferencePointCollection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13fe1-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13fe1-110">Referencia a una [**\_ colección CIM**](cim-collection.md) que representa la colección de puntos de referencia que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="13fe1-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="13fe1-111">*ExportDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13fe1-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13fe1-112">Ruta de acceso completa del directorio al que se va a exportar la colección de puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="13fe1-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="13fe1-113">*ExportSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13fe1-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13fe1-114">Instancia de [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) que representa la configuración de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="13fe1-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="13fe1-115">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13fe1-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13fe1-116">Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="13fe1-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="13fe1-117">Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="13fe1-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13fe1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13fe1-118">Return value</span></span>

<span data-ttu-id="13fe1-119">Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="13fe1-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="13fe1-120">Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del trabajo se puede usar para realizar el seguimiento del progreso de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="13fe1-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="13fe1-121">Cualquier otro valor devuelto indica un error.</span><span class="sxs-lookup"><span data-stu-id="13fe1-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="13fe1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13fe1-122">Requirements</span></span>



| <span data-ttu-id="13fe1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13fe1-123">Requirement</span></span> | <span data-ttu-id="13fe1-124">Value</span><span class="sxs-lookup"><span data-stu-id="13fe1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fe1-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13fe1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13fe1-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="13fe1-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="13fe1-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13fe1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13fe1-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="13fe1-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="13fe1-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13fe1-129">Namespace</span></span><br/>                | <span data-ttu-id="13fe1-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="13fe1-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13fe1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="13fe1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13fe1-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13fe1-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13fe1-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13fe1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13fe1-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13fe1-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13fe1-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="13fe1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fe1-136">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="13fe1-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




