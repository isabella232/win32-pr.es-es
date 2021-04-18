---
description: El método configure envía la información de configuración utilizada para una captura.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Método IDelaydCConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496990"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="b511b-103">IDelaydC:: Configure (método)</span><span class="sxs-lookup"><span data-stu-id="b511b-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="b511b-104">El método **Configure** envía la información de configuración utilizada para una captura.</span><span class="sxs-lookup"><span data-stu-id="b511b-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b511b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b511b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b511b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b511b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b511b-107">*hConfigurationBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b511b-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b511b-108">Identificador del BLOB que contiene la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="b511b-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="b511b-109">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b511b-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b511b-110">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="b511b-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="b511b-111">Para obtener información sobre el contenido de un BLOB de error, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="b511b-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b511b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b511b-112">Return value</span></span>

<span data-ttu-id="b511b-113">Si este método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b511b-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b511b-114">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="b511b-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b511b-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b511b-115">Return code</span></span>                                                                                                      | <span data-ttu-id="b511b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b511b-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b511b-117"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="b511b-118">El NPP informa de que se ha iniciado la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="b511b-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="b511b-119"><dt>**\_disco NMERR \_ no \_ local \_ fijo**</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="b511b-120"><dt>**NMERR \_ \_ no pudo \_ crear la \_ memoria**</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="b511b-121"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="b511b-122">No había memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="b511b-122">No memory was available.</span></span> <span data-ttu-id="b511b-123">Cierre Windows para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="b511b-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="b511b-124"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="b511b-125">El BLOB de configuración especificado por el parámetro hConfiguration no es válido.</span><span class="sxs-lookup"><span data-stu-id="b511b-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b511b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b511b-126">Remarks</span></span>

<span data-ttu-id="b511b-127">Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido, pero no está desconectado.</span><span class="sxs-lookup"><span data-stu-id="b511b-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="b511b-128">El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="b511b-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="b511b-129">El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="b511b-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="b511b-130">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="b511b-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="b511b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b511b-131">Requirements</span></span>



| <span data-ttu-id="b511b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b511b-132">Requirement</span></span> | <span data-ttu-id="b511b-133">Value</span><span class="sxs-lookup"><span data-stu-id="b511b-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b511b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b511b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b511b-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b511b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b511b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b511b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b511b-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b511b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b511b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b511b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b511b-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b511b-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b511b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b511b-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b511b-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b511b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b511b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b511b-143">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="b511b-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="b511b-144">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="b511b-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="b511b-145">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="b511b-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="b511b-146">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="b511b-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




