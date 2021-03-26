---
description: Indica si una dirección de red se ajusta a un tipo y formato especificados.
title: Mensaje de NCM_GETADDRESS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984599"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="9e469-103">NCM el \_ mensaje GETADDRESS</span><span class="sxs-lookup"><span data-stu-id="9e469-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="9e469-104">Indica si una dirección de red se ajusta a un tipo y formato especificados.</span><span class="sxs-lookup"><span data-stu-id="9e469-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="9e469-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e469-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e469-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e469-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e469-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e469-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e469-108">*PV* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9e469-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="9e469-109">Puntero a una estructura de <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> para recibir información de dirección de red en formato analizado, si se valida el formato de dirección y el tipo del control especificado por *hWnd* .</span><span class="sxs-lookup"><span data-stu-id="9e469-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="9e469-110">La aplicación que realiza la llamada es responsable de asignar la memoria para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="9e469-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e469-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e469-111">Return value</span></span>

<span data-ttu-id="9e469-112">Devuelve uno de los siguientes valores de tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9e469-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="9e469-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9e469-113">Return code</span></span>                                                                                                | <span data-ttu-id="9e469-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e469-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e469-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9e469-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="9e469-116">La aplicación que realiza la llamada no pudo asignar una estructura de [**\_ direcciones de NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .</span><span class="sxs-lookup"><span data-stu-id="9e469-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="9e469-117"><dt>**ERROR \_ de \_ búfer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="9e469-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="9e469-118">El búfer de salida es demasiado pequeño para contener la dirección de red analizada.</span><span class="sxs-lookup"><span data-stu-id="9e469-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="9e469-119"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="9e469-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="9e469-120">La cadena de dirección de red no es de ningún tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="9e469-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="9e469-121"><dt>**ERROR \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9e469-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="9e469-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9e469-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="9e469-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9e469-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="9e469-124">No hay ninguna dirección en el control de dirección de red para validar.</span><span class="sxs-lookup"><span data-stu-id="9e469-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="9e469-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e469-125">Remarks</span></span>

<span data-ttu-id="9e469-126">Use el mensaje de **NCM \_ GETADDRESS** para validar una dirección de red en un control de dirección de red con una máscara de tipo de dirección de red preestablecida.</span><span class="sxs-lookup"><span data-stu-id="9e469-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="9e469-127">Para crear una instancia de, use la clase **msctls \_ netaddress** definida en ShellAPI. h.</span><span class="sxs-lookup"><span data-stu-id="9e469-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="9e469-128">Llame a [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) en tiempo de ejecución antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e469-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="9e469-129">Esto inicializa la biblioteca de controles comunes que contiene el control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="9e469-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="9e469-130">Este mensaje obtiene la cadena de dirección de red de un control de dirección de red, analiza la cadena y comprueba si la cadena coincide con una máscara de tipo de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="9e469-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="9e469-131">Si la cadena coincide con la máscara, el mensaje devuelve S \_ OK y devuelve la cadena en forma de análisis a la aplicación que realiza la llamada (incluido el número de puerto, la longitud del prefijo y otra información de dirección), mediante la estructura de la [**\_ dirección de NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) a la que apunta *PV*.</span><span class="sxs-lookup"><span data-stu-id="9e469-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="9e469-132">Este mensaje devuelve E \_ INVALIDARG si la aplicación que realiza la llamada no puede asignar la estructura a la que apunta *PV*.</span><span class="sxs-lookup"><span data-stu-id="9e469-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="9e469-133">Se analizan las representaciones de las versiones 4 y 6 (V4/V6) de la dirección del Protocolo de Internet (IP) para servicios y redes, así como las direcciones de Internet con nombre y los servicios que usan el formato del sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="9e469-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="9e469-134">Si la cadena de la dirección de red representa un nombre de host (DNS) o servicio con nombre, el valor devuelto en el miembro **PrefixLength** de la [**\_ Dirección NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) es cero.</span><span class="sxs-lookup"><span data-stu-id="9e469-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="9e469-135">Establezca la máscara de tipo de dirección de red mediante el mensaje [**\_ SETALLOWTYPE de NCM**](ncm-setallowtype.md) antes de enviar la macro **NCM \_ GETADDRESS** .</span><span class="sxs-lookup"><span data-stu-id="9e469-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e469-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e469-136">Requirements</span></span>



| <span data-ttu-id="9e469-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e469-137">Requirement</span></span> | <span data-ttu-id="9e469-138">Value</span><span class="sxs-lookup"><span data-stu-id="9e469-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e469-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e469-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9e469-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e469-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e469-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e469-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9e469-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e469-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e469-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e469-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e469-144"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e469-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e469-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e469-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e469-146">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="9e469-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="9e469-147">**NetAddr \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="9e469-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




