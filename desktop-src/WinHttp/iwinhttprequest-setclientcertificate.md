---
description: Selecciona un certificado de cliente para enviar a un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'IWinHttpRequest:: SetClientCertificate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361040"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="20b20-103">IWinHttpRequest:: SetClientCertificate (método)</span><span class="sxs-lookup"><span data-stu-id="20b20-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="20b20-104">El método **SetClientCertificate** selecciona un certificado de cliente para enviarlo a un servidor de protocolo seguro de transferencia de hipertexto (https).</span><span class="sxs-lookup"><span data-stu-id="20b20-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20b20-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="20b20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20b20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20b20-107">*ClientCertificate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20b20-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b20-108">Especifica la ubicación, el [*almacén de certificados*](glossary.md)y el asunto de un certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="20b20-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20b20-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20b20-109">Return value</span></span>

<span data-ttu-id="20b20-110">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="20b20-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="20b20-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20b20-111">Remarks</span></span>

<span data-ttu-id="20b20-112">La cadena especificada en el parámetro *ClientCertificate* consta de la ubicación del certificado, el almacén de certificados y el nombre de sujeto delimitados por barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="20b20-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="20b20-113">Para obtener más información acerca de los componentes de la cadena de certificado, consulte [certificados de cliente](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="20b20-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="20b20-114">El nombre y la ubicación del almacén de certificados son opcionales.</span><span class="sxs-lookup"><span data-stu-id="20b20-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="20b20-115">Sin embargo, si especifica un almacén de certificados, también debe especificar la ubicación del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="20b20-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="20b20-116">La ubicación predeterminada es \_ usuario actual y el almacén de certificados predeterminado es "My".</span><span class="sxs-lookup"><span data-stu-id="20b20-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="20b20-117">Un asunto en blanco indica que se debe usar el primer certificado del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="20b20-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="20b20-118">Llame a **SetClientCertificate** para seleccionar un certificado antes de llamar a [**send**](iwinhttprequest-send.md) para enviar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="20b20-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="20b20-119">Los servicios HTTP de Microsoft Windows (WinHTTP) no proporcionan certificados de cliente a los servidores proxy que solicitan certificados para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="20b20-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="20b20-120">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="20b20-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="20b20-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="20b20-121">Examples</span></span>

<span data-ttu-id="20b20-122">En el ejemplo de scripting siguiente se muestra cómo seleccionar un certificado de cliente para enviarlo con una solicitud.</span><span class="sxs-lookup"><span data-stu-id="20b20-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="20b20-123">Se elige un certificado con el asunto "My Middle-Tier Certificate" en el almacén de certificados "personal" del registro en **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="20b20-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="20b20-124">Dado que este ejemplo de código es específico de Microsoft JScript, que usa la barra diagonal inversa como carácter de escape, se requieren dos barras diagonales inversas adyacentes para delimitar los componentes de la cadena de certificado.</span><span class="sxs-lookup"><span data-stu-id="20b20-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="20b20-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20b20-125">Requirements</span></span>



| <span data-ttu-id="20b20-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="20b20-126">Requirement</span></span> | <span data-ttu-id="20b20-127">Value</span><span class="sxs-lookup"><span data-stu-id="20b20-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b20-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20b20-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20b20-129">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="20b20-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="20b20-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20b20-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20b20-131">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="20b20-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="20b20-132">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="20b20-132">Redistributable</span></span><br/>          | <span data-ttu-id="20b20-133">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="20b20-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="20b20-134">IDL</span><span class="sxs-lookup"><span data-stu-id="20b20-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20b20-135"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20b20-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="20b20-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20b20-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="20b20-137"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20b20-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="20b20-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="20b20-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b20-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b20-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20b20-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="20b20-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b20-141">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="20b20-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="20b20-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="20b20-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="20b20-143">SSL en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="20b20-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="20b20-144">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="20b20-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




