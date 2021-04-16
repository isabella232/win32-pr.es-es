---
description: Solicita un extremo que se utiliza para conectarse a un servicio.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'IUpdateEndpointProvider:: GetServiceEndpoint (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686856"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="fb51e-103">IUpdateEndpointProvider:: GetServiceEndpoint (método)</span><span class="sxs-lookup"><span data-stu-id="fb51e-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="fb51e-104">Solicita un extremo que se utiliza para conectarse a un servicio.</span><span class="sxs-lookup"><span data-stu-id="fb51e-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb51e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb51e-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="fb51e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb51e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb51e-107">*ServiceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb51e-108">Identifica el servicio que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="fb51e-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="fb51e-109">*endpointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb51e-110">Identifica el tipo de extremo implementado por el servicio.</span><span class="sxs-lookup"><span data-stu-id="fb51e-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="fb51e-111">La enumeración [**UpdateEndpointType**](updateendpointtype.md) define las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="fb51e-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="fb51e-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="fb51e-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="fb51e-113">Un punto de conexión cliente-servidor que se utiliza para conectarse al servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="fb51e-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="fb51e-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="fb51e-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="fb51e-115">Un punto de conexión de informes que se utiliza cuando el cliente informa de los resultados de los análisis, las descargas y vuelve a instalarse en el servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="fb51e-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="fb51e-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="fb51e-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="fb51e-117">Un punto de conexión de Self-Update que se utiliza cuando el equipo cliente se pone en contacto con un servicio de actualización para comprobar si hay una nueva versión del software cliente del agente de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="fb51e-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="fb51e-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="fb51e-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="fb51e-119">Un punto de conexión de Reglamento que se utiliza cuando el equipo cliente se pone en contacto con el servicio de Reglamento para actuar sobre una actualización determinada que es aplicable al equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="fb51e-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="fb51e-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="fb51e-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="fb51e-121">Un Simple-Targeting endoint que solo se usa con servicios privados (servidores WSUS en entornos corporativos).</span><span class="sxs-lookup"><span data-stu-id="fb51e-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fb51e-122">*proxySettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb51e-123">Identifica la configuración que se usa al conectarse a un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="fb51e-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="fb51e-124">*hUserToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb51e-125">Contiene un objeto de identificador de token que representa al usuario.</span><span class="sxs-lookup"><span data-stu-id="fb51e-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="fb51e-126">El proveedor de puntos de conexión usa este token para determinar qué configuración de proxy y credenciales usar.</span><span class="sxs-lookup"><span data-stu-id="fb51e-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="fb51e-127">*fRefreshOnline* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb51e-128">Indica que el WUA meteorológico solicita un nuevo token.</span><span class="sxs-lookup"><span data-stu-id="fb51e-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="fb51e-129">True indica que se solicita un token nuevo.</span><span class="sxs-lookup"><span data-stu-id="fb51e-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="fb51e-130">False indica que se solicita un token nuevo o almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="fb51e-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="fb51e-131">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fb51e-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="fb51e-132">*pbstrEndpointLoc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb51e-133">Especifique la dirección URL que se usa para comunicarse con el servicio.</span><span class="sxs-lookup"><span data-stu-id="fb51e-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="fb51e-134">Por ejemplo, para un punto de conexión de cliente-Server sería la dirección URL del servicio de servidor de cliente.</span><span class="sxs-lookup"><span data-stu-id="fb51e-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="fb51e-135">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fb51e-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb51e-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb51e-136">Return value</span></span>

<span data-ttu-id="fb51e-137">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="fb51e-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="fb51e-138">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="fb51e-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb51e-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb51e-139">Remarks</span></span>

<span data-ttu-id="fb51e-140">WUA normalmente establece el parámetro *fRefreshOnline* en false cuando se llama por primera vez a este método y, después, si se produce un error de conexión, WUA establece ese parámetro en true cuando se llama de nuevo al método.</span><span class="sxs-lookup"><span data-stu-id="fb51e-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="fb51e-141">Sin embargo, la implementación de este método puede solicitar un nuevo token de un servicio de token de seguridad (STS) o proporcionar un token almacenado en caché en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="fb51e-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="fb51e-142">Si el extremo no necesita autenticación, el autor de la llamada puede conectarse al servicio usando solo la dirección URL especificada por el parámetro *pbstrEndpointLoc* .</span><span class="sxs-lookup"><span data-stu-id="fb51e-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="fb51e-143">Si el extremo requiere autenticación, el autor de la llamada puede usar la dirección URL especificada por el parámetro *pbstrEndpointLoc* y los datos proporcionados por los demás parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb51e-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb51e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb51e-144">Requirements</span></span>



| <span data-ttu-id="fb51e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb51e-145">Requirement</span></span> | <span data-ttu-id="fb51e-146">Value</span><span class="sxs-lookup"><span data-stu-id="fb51e-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb51e-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb51e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fb51e-148">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="fb51e-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb51e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fb51e-150">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="fb51e-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fb51e-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb51e-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb51e-152"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb51e-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb51e-153">IDL</span><span class="sxs-lookup"><span data-stu-id="fb51e-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb51e-154"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb51e-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="fb51e-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb51e-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb51e-156"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb51e-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb51e-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb51e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb51e-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb51e-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb51e-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb51e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb51e-160">**IUpdateEndpointProvider**</span><span class="sxs-lookup"><span data-stu-id="fb51e-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 




