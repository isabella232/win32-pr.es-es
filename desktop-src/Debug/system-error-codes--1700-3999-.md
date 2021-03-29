---
description: Describe los códigos de error 1700-3999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Códigos de error del sistema (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907002"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="48db9-103">Códigos de error del sistema (1700-3999)</span><span class="sxs-lookup"><span data-stu-id="48db9-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="48db9-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="48db9-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="48db9-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="48db9-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="48db9-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 1700 a 3999.</span><span class="sxs-lookup"><span data-stu-id="48db9-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="48db9-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="48db9-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="48db9-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="48db9-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="48db9-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_enlace de \_ cadena no válido de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-110">1700 (0x6A4)</span><span class="sxs-lookup"><span data-stu-id="48db9-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-111">El enlace de cadena no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**el \_ \_ \_ tipo \_ de enlace de \_ RPC es incorrecto**</span><span class="sxs-lookup"><span data-stu-id="48db9-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-113">1701 (0x6A5)</span><span class="sxs-lookup"><span data-stu-id="48db9-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-114">El identificador de enlace no es del tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="48db9-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**enlace de RPC \_ S \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-116">1702 (0x6A6)</span><span class="sxs-lookup"><span data-stu-id="48db9-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-117">El identificador de enlace no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**\_PROTSEQ RPC \_ S \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="48db9-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-119">1703 (0x6A7)</span><span class="sxs-lookup"><span data-stu-id="48db9-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-120">No se admite la secuencia de protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S RPC \_ no válida \_ \_ PROTSEQ**</span><span class="sxs-lookup"><span data-stu-id="48db9-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-122">1704 (0x6A8)</span><span class="sxs-lookup"><span data-stu-id="48db9-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-123">La secuencia de protocolo RPC no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_UUID de \_ cadena no válida de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-125">1705 (0x6A9)</span><span class="sxs-lookup"><span data-stu-id="48db9-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-126">El identificador único universal (UUID) de cadena no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_formato de \_ extremo no válido de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-128">1706 (0x6AA)</span><span class="sxs-lookup"><span data-stu-id="48db9-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-129">El formato del extremo no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_dirección de \_ red no válida de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-131">1707 (0x6AB)</span><span class="sxs-lookup"><span data-stu-id="48db9-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-132">La dirección de red no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ no \_ se encontró ningún punto de conexión \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-134">1708 (0x6AC)</span><span class="sxs-lookup"><span data-stu-id="48db9-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-135">No se encontró ningún punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="48db9-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**tiempo de espera de RPC \_ S \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-137">1709 (0x6AD)</span><span class="sxs-lookup"><span data-stu-id="48db9-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-138">El valor de tiempo de espera no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_ \_ \_ no \_ se encontró el objeto RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-140">1710 (0x6AE)</span><span class="sxs-lookup"><span data-stu-id="48db9-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-141">No se encontró el identificador único universal (UUID) del objeto.</span><span class="sxs-lookup"><span data-stu-id="48db9-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ ya \_ registradas**</span><span class="sxs-lookup"><span data-stu-id="48db9-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-143">1711 (0x6AF)</span><span class="sxs-lookup"><span data-stu-id="48db9-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-144">El identificador único universal (UUID) del objeto ya se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="48db9-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**el \_ tipo de RPC S \_ \_ ya está \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="48db9-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-146">1712 (0x6B0)</span><span class="sxs-lookup"><span data-stu-id="48db9-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-147">El identificador único universal (UUID) de tipo ya se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="48db9-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ ya \_ escuchando**</span><span class="sxs-lookup"><span data-stu-id="48db9-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-149">1713 (0x6B1)</span><span class="sxs-lookup"><span data-stu-id="48db9-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-150">El servidor RPC ya está escuchando.</span><span class="sxs-lookup"><span data-stu-id="48db9-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ no \_ PROTSEQS \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="48db9-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-152">1714 (0x6B2)</span><span class="sxs-lookup"><span data-stu-id="48db9-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-153">No se ha registrado ninguna secuencia de protocolo.</span><span class="sxs-lookup"><span data-stu-id="48db9-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ \_ no está \_ escuchando**</span><span class="sxs-lookup"><span data-stu-id="48db9-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-155">1715 (0x6B3)</span><span class="sxs-lookup"><span data-stu-id="48db9-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-156">El servidor RPC no está escuchando.</span><span class="sxs-lookup"><span data-stu-id="48db9-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_tipo de \_ \_ Administrador desconocido \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-158">1716 (0x6B4)</span><span class="sxs-lookup"><span data-stu-id="48db9-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-159">No se conoce el tipo de administrador.</span><span class="sxs-lookup"><span data-stu-id="48db9-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ desconocido \_ si**</span><span class="sxs-lookup"><span data-stu-id="48db9-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-161">1717 (0x6B5)</span><span class="sxs-lookup"><span data-stu-id="48db9-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-162">Se desconoce la interfaz.</span><span class="sxs-lookup"><span data-stu-id="48db9-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ no \_ enlaces**</span><span class="sxs-lookup"><span data-stu-id="48db9-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-164">1718 (0x6B6)</span><span class="sxs-lookup"><span data-stu-id="48db9-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-165">No hay ningún enlace.</span><span class="sxs-lookup"><span data-stu-id="48db9-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ no \_ PROTSEQS**</span><span class="sxs-lookup"><span data-stu-id="48db9-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-167">1719 (0x6B7)</span><span class="sxs-lookup"><span data-stu-id="48db9-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-168">No hay secuencias de protocolo.</span><span class="sxs-lookup"><span data-stu-id="48db9-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC S no se pudo \_ \_ crear el punto de \_ \_ conexión**</span><span class="sxs-lookup"><span data-stu-id="48db9-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-170">1720 (0x6B8)</span><span class="sxs-lookup"><span data-stu-id="48db9-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-171">No se puede crear el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="48db9-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ \_ de \_ recursos**</span><span class="sxs-lookup"><span data-stu-id="48db9-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-173">1721 (0x6B9)</span><span class="sxs-lookup"><span data-stu-id="48db9-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-174">No hay suficientes recursos disponibles para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="48db9-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**el \_ servidor RPC S \_ \_ no está disponible**</span><span class="sxs-lookup"><span data-stu-id="48db9-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-176">1722 (0x6BA)</span><span class="sxs-lookup"><span data-stu-id="48db9-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-177">El servidor RPC no está disponible.</span><span class="sxs-lookup"><span data-stu-id="48db9-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**el servidor de RPC está \_ \_ \_ demasiado \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="48db9-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-179">1723 (0x6BB)</span><span class="sxs-lookup"><span data-stu-id="48db9-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-180">El servidor RPC está demasiado ocupado para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="48db9-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_Opciones de \_ red no válidas de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-182">1724 (0x6BC)</span><span class="sxs-lookup"><span data-stu-id="48db9-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-183">Las opciones de red no son válidas.</span><span class="sxs-lookup"><span data-stu-id="48db9-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ no \_ llamada \_ activa**</span><span class="sxs-lookup"><span data-stu-id="48db9-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-185">1725 (0x6BD)</span><span class="sxs-lookup"><span data-stu-id="48db9-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-186">No hay llamadas a procedimiento remoto activas en este subproceso.</span><span class="sxs-lookup"><span data-stu-id="48db9-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**\_error de \_ llamada RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-188">1726 (0x6BE)</span><span class="sxs-lookup"><span data-stu-id="48db9-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-189">Error en la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="48db9-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**\_error de \_ llamada RPC S \_ \_ DNE**</span><span class="sxs-lookup"><span data-stu-id="48db9-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-191">1727 (0x6BF)</span><span class="sxs-lookup"><span data-stu-id="48db9-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-192">Error en la llamada a procedimiento remoto y no se ejecutó.</span><span class="sxs-lookup"><span data-stu-id="48db9-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_error de \_ Protocolo RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-194">1728 (0x6C0)</span><span class="sxs-lookup"><span data-stu-id="48db9-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-195">Error de protocolo de llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="48db9-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ \_ acceso \_ denegado al proxy RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-197">1729 (0x6C1)</span><span class="sxs-lookup"><span data-stu-id="48db9-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-198">Se denegó el acceso al proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="48db9-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**\_ \_ transacciones no admitidas de RPC S \_ \_ SYN**</span><span class="sxs-lookup"><span data-stu-id="48db9-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-200">1730 (0x6C2)</span><span class="sxs-lookup"><span data-stu-id="48db9-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-201">El servidor RPC no admite la sintaxis de transferencia.</span><span class="sxs-lookup"><span data-stu-id="48db9-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**tipo de RPC \_ \_ no compatible \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-203">1732 (0x6C4)</span><span class="sxs-lookup"><span data-stu-id="48db9-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-204">No se admite el tipo de identificador único universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="48db9-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_etiqueta RPC S \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-206">1733 (0x6C5)</span><span class="sxs-lookup"><span data-stu-id="48db9-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-207">La etiqueta no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC \_ con \_ enlace no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-209">1734 (0x6C6)</span><span class="sxs-lookup"><span data-stu-id="48db9-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-210">Los límites de la matriz no son válidos.</span><span class="sxs-lookup"><span data-stu-id="48db9-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ no \_ nombre de entrada \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-212">1735 (0x6C7)</span><span class="sxs-lookup"><span data-stu-id="48db9-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-213">El enlace no contiene un nombre de entrada.</span><span class="sxs-lookup"><span data-stu-id="48db9-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_Sintaxis de \_ nombre no válida de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-215">1736 (0x6C8)</span><span class="sxs-lookup"><span data-stu-id="48db9-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-216">La sintaxis del nombre no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_Sintaxis de \_ nombre no compatible de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-218">1737 (0x6C9)</span><span class="sxs-lookup"><span data-stu-id="48db9-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-219">No se admite la sintaxis de nombre.</span><span class="sxs-lookup"><span data-stu-id="48db9-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_ \_ UUID \_ no \_ dirección de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-221">1739 (0x6CB)</span><span class="sxs-lookup"><span data-stu-id="48db9-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-222">No hay ninguna dirección de red disponible para crear un identificador único universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="48db9-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ \_ extremo duplicado de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-224">1740 (0x6CC)</span><span class="sxs-lookup"><span data-stu-id="48db9-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-225">El punto de conexión es un duplicado.</span><span class="sxs-lookup"><span data-stu-id="48db9-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_tipo de \_ \_ autenticación desconocida \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-227">1741 (0x6CD)</span><span class="sxs-lookup"><span data-stu-id="48db9-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-228">Se desconoce el tipo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="48db9-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**llamadas de RPC \_ S \_ Max \_ \_ demasiado \_ pequeñas**</span><span class="sxs-lookup"><span data-stu-id="48db9-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-230">1742 (0x6CE)</span><span class="sxs-lookup"><span data-stu-id="48db9-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-231">El número máximo de llamadas es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="48db9-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**la \_ cadena de RPC \_ \_ es demasiado \_ larga**</span><span class="sxs-lookup"><span data-stu-id="48db9-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-233">1743 (0x6CF)</span><span class="sxs-lookup"><span data-stu-id="48db9-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-234">La cadena es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="48db9-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**\_ \_ \_ no \_ se encontró RPC S PROTSEQ**</span><span class="sxs-lookup"><span data-stu-id="48db9-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-236">1744 (0x6D0)</span><span class="sxs-lookup"><span data-stu-id="48db9-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-237">No se encontró la secuencia de protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**\_ \_ PROCNUM de RPC S \_ fuera \_ del \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="48db9-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-239">1745 (0x6D1)</span><span class="sxs-lookup"><span data-stu-id="48db9-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-240">El número de procedimiento está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="48db9-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**el \_ enlace de RPC S \_ \_ \_ no tiene \_ autenticación**</span><span class="sxs-lookup"><span data-stu-id="48db9-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-242">1746 (0x6D2)</span><span class="sxs-lookup"><span data-stu-id="48db9-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-243">El enlace no contiene información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="48db9-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_servicio de \_ \_ autenticación desconocido \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-245">1747 (0x6D3)</span><span class="sxs-lookup"><span data-stu-id="48db9-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-246">Se desconoce el servicio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="48db9-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_nivel de \_ \_ autenticación desconocida \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-248">1748 (0x6D4)</span><span class="sxs-lookup"><span data-stu-id="48db9-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-249">Se desconoce el nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="48db9-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_identidad de \_ autenticación no válida de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-251">1749 (0x6D5)</span><span class="sxs-lookup"><span data-stu-id="48db9-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-252">El contexto de seguridad no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC \_ S \_ \_ servicio desconocido AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-254">1750 (0x6D6)</span><span class="sxs-lookup"><span data-stu-id="48db9-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-255">Se desconoce el servicio de autorización.</span><span class="sxs-lookup"><span data-stu-id="48db9-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_ \_ entrada no válida de EPT S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-257">1751 (0x6D7)</span><span class="sxs-lookup"><span data-stu-id="48db9-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-258">La entrada no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT S no se pudo \_ \_ realizar la \_ \_ operación**</span><span class="sxs-lookup"><span data-stu-id="48db9-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-260">1752 (0x6D8)</span><span class="sxs-lookup"><span data-stu-id="48db9-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-261">El punto de conexión de servidor no puede realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="48db9-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ no \_ registrada**</span><span class="sxs-lookup"><span data-stu-id="48db9-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-263">1753 (0x6D9)</span><span class="sxs-lookup"><span data-stu-id="48db9-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-264">no hay más puntos de conexión disponibles desde el asignador de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="48db9-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**no \_ \_ hay nada \_ para \_ exportar en RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-266">1754 (0x6DA)</span><span class="sxs-lookup"><span data-stu-id="48db9-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-267">No se ha exportado ninguna interfaz.</span><span class="sxs-lookup"><span data-stu-id="48db9-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ nombre incompleto de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-269">1755 (0x6DB)</span><span class="sxs-lookup"><span data-stu-id="48db9-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-270">El nombre de la entrada está incompleto.</span><span class="sxs-lookup"><span data-stu-id="48db9-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ opción no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-272">1756 (0x6DC)</span><span class="sxs-lookup"><span data-stu-id="48db9-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-273">La opción de versión no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ no hay \_ más \_ miembros**</span><span class="sxs-lookup"><span data-stu-id="48db9-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-275">1757 (0x6DD)</span><span class="sxs-lookup"><span data-stu-id="48db9-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-276">No hay más miembros.</span><span class="sxs-lookup"><span data-stu-id="48db9-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**\_ \_ no todos los obj de RPC no se \_ \_ \_ exportaron**</span><span class="sxs-lookup"><span data-stu-id="48db9-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-278">1758 (0x6DE)</span><span class="sxs-lookup"><span data-stu-id="48db9-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-279">No hay nada que desexportar.</span><span class="sxs-lookup"><span data-stu-id="48db9-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_ \_ \_ no \_ se encuentra la interfaz RPC**</span><span class="sxs-lookup"><span data-stu-id="48db9-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-281">1759 (0x6DF)</span><span class="sxs-lookup"><span data-stu-id="48db9-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-282">No se encontró la interfaz.</span><span class="sxs-lookup"><span data-stu-id="48db9-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**la \_ entrada RPC S \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48db9-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-284">1760 (0x6E0)</span><span class="sxs-lookup"><span data-stu-id="48db9-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-285">La entrada ya existe.</span><span class="sxs-lookup"><span data-stu-id="48db9-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_ \_ \_ no \_ se encontró la entrada RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-287">1761 (0x6E1)</span><span class="sxs-lookup"><span data-stu-id="48db9-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-288">No se encuentra la entrada.</span><span class="sxs-lookup"><span data-stu-id="48db9-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**servicio de nombres de RPC \_ \_ \_ \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="48db9-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-290">1762 (0x6E2)</span><span class="sxs-lookup"><span data-stu-id="48db9-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-291">El servicio de nombres no está disponible.</span><span class="sxs-lookup"><span data-stu-id="48db9-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_identificador de \_ NAF no válido de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-293">1763 (0x6E3)</span><span class="sxs-lookup"><span data-stu-id="48db9-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-294">La familia de direcciones de red no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ no \_ admite**</span><span class="sxs-lookup"><span data-stu-id="48db9-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-296">1764 (0x6E4)</span><span class="sxs-lookup"><span data-stu-id="48db9-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-297">No se admite la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S \_ no hay \_ contexto \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="48db9-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-299">1765 (0x6E5)</span><span class="sxs-lookup"><span data-stu-id="48db9-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-300">No hay ningún contexto de seguridad disponible para permitir la suplantación.</span><span class="sxs-lookup"><span data-stu-id="48db9-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ error interno de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-302">1766 (0x6E6)</span><span class="sxs-lookup"><span data-stu-id="48db9-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-303">Se produjo un error interno en una llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="48db9-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**División de RPC \_ S \_ cero \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-305">1767 (0x6E7)</span><span class="sxs-lookup"><span data-stu-id="48db9-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-306">El servidor RPC intentó una división de enteros por cero.</span><span class="sxs-lookup"><span data-stu-id="48db9-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_error de \_ dirección de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-308">1768 (0x6E8)</span><span class="sxs-lookup"><span data-stu-id="48db9-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-309">Se produjo un error de direccionamiento en el servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_ \_ \_ valor cero de FP de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-311">1769 (0x6E9)</span><span class="sxs-lookup"><span data-stu-id="48db9-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-312">Una operación de punto flotante en el servidor RPC provocó una división por cero.</span><span class="sxs-lookup"><span data-stu-id="48db9-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**subdesbordamiento de FP de RPC \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-314">1770 (0x6EA)</span><span class="sxs-lookup"><span data-stu-id="48db9-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-315">Se produjo un subdesbordamiento de punto flotante en el servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_desbordamiento de \_ FP de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-317">1771 (0x6EB)</span><span class="sxs-lookup"><span data-stu-id="48db9-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-318">Se produjo un desbordamiento de punto flotante en el servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**\_ \_ no hay \_ más \_ entradas de RPC X**</span><span class="sxs-lookup"><span data-stu-id="48db9-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-320">1772 (0x6EC)</span><span class="sxs-lookup"><span data-stu-id="48db9-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-321">Se ha agotado la lista de servidores RPC disponibles para el enlace de identificadores automáticos.</span><span class="sxs-lookup"><span data-stu-id="48db9-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**error de apertura de transacciones de RPC \_ X \_ SS \_ Char \_ Trans \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-323">1773 (0x6ED)</span><span class="sxs-lookup"><span data-stu-id="48db9-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-324">No se puede abrir el archivo de tabla de traducción de caracteres.</span><span class="sxs-lookup"><span data-stu-id="48db9-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**archivo corto de trans. de RPC \_ X \_ SS \_ Char \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-326">1774 (0x6EE)</span><span class="sxs-lookup"><span data-stu-id="48db9-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-327">El archivo que contiene la tabla de traducción de caracteres tiene menos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="48db9-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ en \_ \_ contexto nulo**</span><span class="sxs-lookup"><span data-stu-id="48db9-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-329">1775 (0x6EF)</span><span class="sxs-lookup"><span data-stu-id="48db9-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-330">Se pasó un identificador de contexto nulo desde el cliente al host durante una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="48db9-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**contexto de RPC \_ X \_ SS \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="48db9-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-332">1777 (0x6F1)</span><span class="sxs-lookup"><span data-stu-id="48db9-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-333">El identificador de contexto cambió durante una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="48db9-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**\_ \_ \_ no coinciden los identificadores de RPC X SS \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-335">1778 (0x6F2)</span><span class="sxs-lookup"><span data-stu-id="48db9-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-336">Los identificadores de enlace pasados a una llamada a procedimiento remoto no coinciden.</span><span class="sxs-lookup"><span data-stu-id="48db9-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ no puede \_ obtener el \_ identificador de llamada \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-338">1779 (0x6F3)</span><span class="sxs-lookup"><span data-stu-id="48db9-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-339">El código auxiliar no puede obtener el identificador de llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="48db9-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_puntero de \_ \_ referencia null \_ de RPC X**</span><span class="sxs-lookup"><span data-stu-id="48db9-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-341">1780 (0x6F4)</span><span class="sxs-lookup"><span data-stu-id="48db9-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-342">Se pasó un puntero de referencia nulo al código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="48db9-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_ \_ valor de enumeración de RPC X \_ \_ fuera \_ del \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="48db9-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-344">1781 (0x6F5)</span><span class="sxs-lookup"><span data-stu-id="48db9-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-345">El valor de la enumeración está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="48db9-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**el \_ número de bytes de RPC X \_ \_ \_ es demasiado \_ pequeño**</span><span class="sxs-lookup"><span data-stu-id="48db9-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-347">1782 (0x6F6)</span><span class="sxs-lookup"><span data-stu-id="48db9-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-348">El recuento de bytes es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="48db9-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**\_datos de \_ \_ código auxiliar \_ de RPC X incorrecto**</span><span class="sxs-lookup"><span data-stu-id="48db9-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-350">1783 (0x6F7)</span><span class="sxs-lookup"><span data-stu-id="48db9-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-351">El código auxiliar ha recibido datos incorrectos.</span><span class="sxs-lookup"><span data-stu-id="48db9-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR \_ de \_ búfer de usuario no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-353">1784 (0x6F8)</span><span class="sxs-lookup"><span data-stu-id="48db9-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-354">El búfer de usuario proporcionado no es válido para la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR de \_ medios no reconocidos \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-356">1785 (0x6F9)</span><span class="sxs-lookup"><span data-stu-id="48db9-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-357">No se reconoce el medio de disco.</span><span class="sxs-lookup"><span data-stu-id="48db9-357">The disk media is not recognized.</span></span> <span data-ttu-id="48db9-358">Es posible que no tenga formato.</span><span class="sxs-lookup"><span data-stu-id="48db9-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**NO se pudo \_ \_ confiar en \_ \_ secreto LSA**</span><span class="sxs-lookup"><span data-stu-id="48db9-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-360">1786 (0x6FA)</span><span class="sxs-lookup"><span data-stu-id="48db9-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-361">La estación de trabajo no tiene un secreto de confianza.</span><span class="sxs-lookup"><span data-stu-id="48db9-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**NO se pudo tener la \_ \_ \_ cuenta SAM de confianza \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-363">1787 (0x6FB)</span><span class="sxs-lookup"><span data-stu-id="48db9-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-364">La base de datos de seguridad del servidor no tiene una cuenta de equipo para esta relación de confianza de estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="48db9-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR \_ de \_ dominio de confianza \_ erróneo**</span><span class="sxs-lookup"><span data-stu-id="48db9-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-366">1788 (0x6FC)</span><span class="sxs-lookup"><span data-stu-id="48db9-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-367">Error en la relación de confianza entre el dominio principal y el dominio en el que se confía.</span><span class="sxs-lookup"><span data-stu-id="48db9-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR de \_ relación de confianza error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-369">1789 (0x6FD)</span><span class="sxs-lookup"><span data-stu-id="48db9-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-370">Error en la relación de confianza entre esta estación de trabajo y el dominio principal.</span><span class="sxs-lookup"><span data-stu-id="48db9-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR de \_ confianza \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-372">1790 (0x6FE)</span><span class="sxs-lookup"><span data-stu-id="48db9-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-373">Error de inicio de sesión de red.</span><span class="sxs-lookup"><span data-stu-id="48db9-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_ \_ llamada de RPC S \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="48db9-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-375">1791 (0x6FF)</span><span class="sxs-lookup"><span data-stu-id="48db9-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-376">Ya hay una llamada a procedimiento remoto en curso para este subproceso.</span><span class="sxs-lookup"><span data-stu-id="48db9-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR \_ Netlogon \_ no \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="48db9-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-378">1792 (0x700)</span><span class="sxs-lookup"><span data-stu-id="48db9-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-379">Se intentó iniciar sesión, pero no se inició el servicio de inicio de sesión de red.</span><span class="sxs-lookup"><span data-stu-id="48db9-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**cuenta de ERROR \_ \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="48db9-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-381">1793 (0x701)</span><span class="sxs-lookup"><span data-stu-id="48db9-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-382">La cuenta del usuario expiró.</span><span class="sxs-lookup"><span data-stu-id="48db9-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**el \_ REdirector de errores \_ tiene \_ \_ identificadores abiertos**</span><span class="sxs-lookup"><span data-stu-id="48db9-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-384">1794 (0x702)</span><span class="sxs-lookup"><span data-stu-id="48db9-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-385">El redirector está en uso y no se puede descargar.</span><span class="sxs-lookup"><span data-stu-id="48db9-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**controlador de impresora de ERROR \_ \_ \_ ya \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="48db9-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-387">1795 (0x703)</span><span class="sxs-lookup"><span data-stu-id="48db9-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-388">El controlador de impresora especificado ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="48db9-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR \_ de \_ Puerto desconocido**</span><span class="sxs-lookup"><span data-stu-id="48db9-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-390">1796 (0x704)</span><span class="sxs-lookup"><span data-stu-id="48db9-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-391">El puerto especificado es desconocido.</span><span class="sxs-lookup"><span data-stu-id="48db9-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR \_ de \_ controlador de impresora desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-393">1797 (0x705)</span><span class="sxs-lookup"><span data-stu-id="48db9-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-394">Se desconoce el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="48db9-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR \_ desconocido \_ PRINTPROCESSOR**</span><span class="sxs-lookup"><span data-stu-id="48db9-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-396">1798 (0x706)</span><span class="sxs-lookup"><span data-stu-id="48db9-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-397">Se desconoce el procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="48db9-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR \_ de \_ archivo de separador no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-399">1799 (0x707)</span><span class="sxs-lookup"><span data-stu-id="48db9-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-400">El archivo de separador especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR \_ de \_ prioridad no válida**</span><span class="sxs-lookup"><span data-stu-id="48db9-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-402">1800 (0x708)</span><span class="sxs-lookup"><span data-stu-id="48db9-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-403">La prioridad especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR \_ de \_ nombre de impresora no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-405">1801 (0x709)</span><span class="sxs-lookup"><span data-stu-id="48db9-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-406">El nombre de la impresora no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**la \_ impresora de error \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48db9-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-408">1802 (0x70A)</span><span class="sxs-lookup"><span data-stu-id="48db9-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-409">La impresora ya existe.</span><span class="sxs-lookup"><span data-stu-id="48db9-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR \_ de \_ comando de impresora no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-411">1803 (0x70B)</span><span class="sxs-lookup"><span data-stu-id="48db9-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-412">El comando de impresora no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR de tipo de mensaje \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-414">1804 (0x70C)</span><span class="sxs-lookup"><span data-stu-id="48db9-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-415">El tipo de parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR \_ de \_ entorno no válido**</span><span class="sxs-lookup"><span data-stu-id="48db9-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-417">1805 (0x70D)</span><span class="sxs-lookup"><span data-stu-id="48db9-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-418">El entorno especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**\_ \_ faltan \_ \_ enlaces de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-420">1806 (0x70E)</span><span class="sxs-lookup"><span data-stu-id="48db9-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-421">No hay más enlaces.</span><span class="sxs-lookup"><span data-stu-id="48db9-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR \_ NOlogo de la \_ cuenta de confianza entre dominios \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-423">1807 (0x70F)</span><span class="sxs-lookup"><span data-stu-id="48db9-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-424">La cuenta usada es una cuenta de confianza entre dominios.</span><span class="sxs-lookup"><span data-stu-id="48db9-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="48db9-425">Use la cuenta de usuario global o la cuenta de usuario local para tener acceso a este servidor.</span><span class="sxs-lookup"><span data-stu-id="48db9-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR # \_ cuenta de \_ confianza de estación de trabajo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-427">1808 (0x710)</span><span class="sxs-lookup"><span data-stu-id="48db9-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-428">La cuenta usada es una cuenta de equipo.</span><span class="sxs-lookup"><span data-stu-id="48db9-428">The account used is a computer account.</span></span> <span data-ttu-id="48db9-429">Use la cuenta de usuario global o la cuenta de usuario local para tener acceso a este servidor.</span><span class="sxs-lookup"><span data-stu-id="48db9-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR \_ NOlogon \_ \_ cuenta de confianza de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-431">1809 (0x711)</span><span class="sxs-lookup"><span data-stu-id="48db9-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-432">La cuenta usada es una cuenta de confianza de servidor.</span><span class="sxs-lookup"><span data-stu-id="48db9-432">The account used is a server trust account.</span></span> <span data-ttu-id="48db9-433">Use la cuenta de usuario global o la cuenta de usuario local para tener acceso a este servidor.</span><span class="sxs-lookup"><span data-stu-id="48db9-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR \_ de \_ confianza de dominio \_ incoherente**</span><span class="sxs-lookup"><span data-stu-id="48db9-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-435">1810 (0x712)</span><span class="sxs-lookup"><span data-stu-id="48db9-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-436">El nombre o el identificador de seguridad (SID) del dominio especificado es incoherente con la información de confianza de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="48db9-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**el \_ servidor de errores \_ tiene \_ \_ identificadores abiertos**</span><span class="sxs-lookup"><span data-stu-id="48db9-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-438">1811 (0x713)</span><span class="sxs-lookup"><span data-stu-id="48db9-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-439">El servidor está en uso y no se puede descargar.</span><span class="sxs-lookup"><span data-stu-id="48db9-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**\_ \_ \_ no \_ se encontraron datos de recursos de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-441">1812 (0x714)</span><span class="sxs-lookup"><span data-stu-id="48db9-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-442">El archivo de imagen especificado no contiene una sección de recursos.</span><span class="sxs-lookup"><span data-stu-id="48db9-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_ \_ \_ no \_ se encontró el tipo de recurso de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-444">1813 (0x715)</span><span class="sxs-lookup"><span data-stu-id="48db9-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-445">No se encuentra el tipo de recurso especificado en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="48db9-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ no \_ se encontró el nombre del recurso de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-447">1814 (0x716)</span><span class="sxs-lookup"><span data-stu-id="48db9-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-448">No se encuentra el nombre de recurso especificado en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="48db9-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ no \_ se encontró el idioma del recurso de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-450">1815 (0x717)</span><span class="sxs-lookup"><span data-stu-id="48db9-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-451">No se encuentra el ID. de idioma de recurso especificado en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="48db9-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR: \_ no \_ hay \_ cuota suficiente**</span><span class="sxs-lookup"><span data-stu-id="48db9-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-453">1816 (0x718)</span><span class="sxs-lookup"><span data-stu-id="48db9-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-454">Cuota insuficiente para procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="48db9-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ no \_ interfaces**</span><span class="sxs-lookup"><span data-stu-id="48db9-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-456">1817 (0x719)</span><span class="sxs-lookup"><span data-stu-id="48db9-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-457">No se ha registrado ninguna interfaz.</span><span class="sxs-lookup"><span data-stu-id="48db9-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_llamada RPC \_ S \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="48db9-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-459">1818 (0x71A)</span><span class="sxs-lookup"><span data-stu-id="48db9-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-460">Se canceló la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="48db9-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**enlace de RPC \_ S \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="48db9-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-462">1819 (0x71B)</span><span class="sxs-lookup"><span data-stu-id="48db9-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-463">El identificador de enlace no contiene toda la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="48db9-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**error de comunicación de RPC \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-465">1820 (0x71C)</span><span class="sxs-lookup"><span data-stu-id="48db9-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-466">Error de comunicación durante una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="48db9-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**\_nivel de \_ autenticación no admitido de RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-468">1821 (0x71D)</span><span class="sxs-lookup"><span data-stu-id="48db9-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-469">No se admite el nivel de autenticación solicitado.</span><span class="sxs-lookup"><span data-stu-id="48db9-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**nombre de princ de RPC \_ \_ no \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-471">1822 (0x71E)</span><span class="sxs-lookup"><span data-stu-id="48db9-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-472">No se registró ningún nombre principal.</span><span class="sxs-lookup"><span data-stu-id="48db9-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**ERROR de RPC de RPC \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-474">1823 (0x71F)</span><span class="sxs-lookup"><span data-stu-id="48db9-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-475">El error especificado no es un código de error de Windows RPC válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**solo el UUID de RPC \_ S \_ \_ local \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-477">1824 (0x720)</span><span class="sxs-lookup"><span data-stu-id="48db9-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-478">Se ha asignado un UUID que solo es válido en este equipo.</span><span class="sxs-lookup"><span data-stu-id="48db9-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**\_error de \_ \_ paquete \_ de RPC s s**</span><span class="sxs-lookup"><span data-stu-id="48db9-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-480">1825 (0x721)</span><span class="sxs-lookup"><span data-stu-id="48db9-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-481">Se produjo un error específico del paquete de seguridad.</span><span class="sxs-lookup"><span data-stu-id="48db9-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ \_ no \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="48db9-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-483">1826 (0x722)</span><span class="sxs-lookup"><span data-stu-id="48db9-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-484">No se ha cancelado el subproceso.</span><span class="sxs-lookup"><span data-stu-id="48db9-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**la \_ acción RPC X \_ no válida \_ es \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-486">1827 (0x723)</span><span class="sxs-lookup"><span data-stu-id="48db9-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-487">Operación no válida en el controlador de codificación y descodificación.</span><span class="sxs-lookup"><span data-stu-id="48db9-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**versión de RPC \_ X \_ errónea \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-489">1828 (0x724)</span><span class="sxs-lookup"><span data-stu-id="48db9-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-490">Versión no compatible del paquete de serialización.</span><span class="sxs-lookup"><span data-stu-id="48db9-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_versión de \_ \_ código auxiliar \_ de RPC X incorrecta**</span><span class="sxs-lookup"><span data-stu-id="48db9-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-492">1829 (0x725)</span><span class="sxs-lookup"><span data-stu-id="48db9-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-493">Versión no compatible del código auxiliar de RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_objeto de \_ \_ canalización no válido \_ de RPC X**</span><span class="sxs-lookup"><span data-stu-id="48db9-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-495">1830 (0x726)</span><span class="sxs-lookup"><span data-stu-id="48db9-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-496">El objeto de canalización RPC no es válido o está dañado.</span><span class="sxs-lookup"><span data-stu-id="48db9-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_orden de \_ \_ canalización \_ incorrecto de RPC X**</span><span class="sxs-lookup"><span data-stu-id="48db9-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-498">1831 (0x727)</span><span class="sxs-lookup"><span data-stu-id="48db9-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-499">Se intentó realizar una operación no válida en un objeto de canalización de RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_versión de \_ \_ canalización \_ incorrecta de RPC X**</span><span class="sxs-lookup"><span data-stu-id="48db9-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-501">1832 (0x728)</span><span class="sxs-lookup"><span data-stu-id="48db9-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-502">Versión de canalización RPC no admitida.</span><span class="sxs-lookup"><span data-stu-id="48db9-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**\_error de \_ autenticación de cookies de \_ RPC \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-504">1833 (0x729)</span><span class="sxs-lookup"><span data-stu-id="48db9-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-505">El servidor proxy HTTP rechazó la conexión porque se produjo un error en la autenticación de cookies.</span><span class="sxs-lookup"><span data-stu-id="48db9-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_ \_ \_ \_ no se encontró el miembro \_ del grupo RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-507">1898 (0x76A)</span><span class="sxs-lookup"><span data-stu-id="48db9-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-508">No se encontró el miembro del grupo.</span><span class="sxs-lookup"><span data-stu-id="48db9-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT S no se pudo \_ \_ \_ crear**</span><span class="sxs-lookup"><span data-stu-id="48db9-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-510">1899 (0x76B)</span><span class="sxs-lookup"><span data-stu-id="48db9-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-511">No se pudo crear la entrada de base de datos del asignador de extremos.</span><span class="sxs-lookup"><span data-stu-id="48db9-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_objeto RPC S \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-513">1900 (0x76C)</span><span class="sxs-lookup"><span data-stu-id="48db9-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-514">El identificador único universal (UUID) del objeto es el UUID nulo.</span><span class="sxs-lookup"><span data-stu-id="48db9-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR \_ de \_ hora no válida**</span><span class="sxs-lookup"><span data-stu-id="48db9-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-516">1901 (0x76D)</span><span class="sxs-lookup"><span data-stu-id="48db9-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-517">La hora especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR \_ de \_ nombre de formulario no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-519">1902 (0x76E)</span><span class="sxs-lookup"><span data-stu-id="48db9-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-520">El nombre de formulario especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR \_ de \_ tamaño de formulario no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-522">1903 (0x76F)</span><span class="sxs-lookup"><span data-stu-id="48db9-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-523">El tamaño de formulario especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR \_ ya en \_ espera**</span><span class="sxs-lookup"><span data-stu-id="48db9-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-525">1904 (0x770)</span><span class="sxs-lookup"><span data-stu-id="48db9-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-526">El identificador de impresora especificado ya se está esperando.</span><span class="sxs-lookup"><span data-stu-id="48db9-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR de \_ impresora \_ eliminada**</span><span class="sxs-lookup"><span data-stu-id="48db9-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-528">1905 (0x771)</span><span class="sxs-lookup"><span data-stu-id="48db9-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-529">La impresora especificada se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="48db9-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR \_ de \_ Estado de impresora no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-531">1906 (0x772)</span><span class="sxs-lookup"><span data-stu-id="48db9-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-532">El estado de la impresora no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**el \_ error \_ debe \_ cambiar la contraseña**</span><span class="sxs-lookup"><span data-stu-id="48db9-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-534">1907 (0x773)</span><span class="sxs-lookup"><span data-stu-id="48db9-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-535">Se debe cambiar la contraseña del usuario antes de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="48db9-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**\_ \_ \_ no \_ se encontró el controlador de dominio de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-537">1908 (0x774)</span><span class="sxs-lookup"><span data-stu-id="48db9-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-538">No se encontró el controlador de dominio para este dominio.</span><span class="sxs-lookup"><span data-stu-id="48db9-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**cuenta de ERROR \_ \_ bloqueada \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-540">1909 (0x775)</span><span class="sxs-lookup"><span data-stu-id="48db9-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-541">La cuenta a la que se hace referencia está bloqueada actualmente y es posible que no haya iniciado sesión en.</span><span class="sxs-lookup"><span data-stu-id="48db9-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**o \_ Oxid no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-543">1910 (0x776)</span><span class="sxs-lookup"><span data-stu-id="48db9-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-544">No se encontró el exportador del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**o \_ OID no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-546">1911 (0x777)</span><span class="sxs-lookup"><span data-stu-id="48db9-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-547">No se encontró el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**o \_ un \_ conjunto no válido**</span><span class="sxs-lookup"><span data-stu-id="48db9-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-549">1912 (0x778)</span><span class="sxs-lookup"><span data-stu-id="48db9-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-550">No se encontró el conjunto de solucionador de objetos especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**\_envío de \_ RPC \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="48db9-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-552">1913 (0x779)</span><span class="sxs-lookup"><span data-stu-id="48db9-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-553">Algunos datos permanecen en el búfer de solicitud.</span><span class="sxs-lookup"><span data-stu-id="48db9-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**\_ \_ \_ identificador asincrónico no válido \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-555">1914 (0x77A)</span><span class="sxs-lookup"><span data-stu-id="48db9-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-556">Identificador de llamada a procedimiento remoto asincrónico no válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_llamada asincrónica de RPC S \_ no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-558">1915 (0x77B)</span><span class="sxs-lookup"><span data-stu-id="48db9-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-559">Identificador de llamada RPC asincrónico no válido para esta operación.</span><span class="sxs-lookup"><span data-stu-id="48db9-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_ \_ canalización RPC X \_ cerrada**</span><span class="sxs-lookup"><span data-stu-id="48db9-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-561">1916 (0x77C)</span><span class="sxs-lookup"><span data-stu-id="48db9-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-562">El objeto de canalización RPC ya se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="48db9-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_error de \_ disciplina de canalización RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-564">1917 (0x77D)</span><span class="sxs-lookup"><span data-stu-id="48db9-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-565">La llamada RPC se completó antes de que se procesaran todas las canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="48db9-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_ \_ canalización RPC X \_ vacía**</span><span class="sxs-lookup"><span data-stu-id="48db9-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-567">1918 (0x77E)</span><span class="sxs-lookup"><span data-stu-id="48db9-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-568">No hay más datos disponibles de la canalización de RPC.</span><span class="sxs-lookup"><span data-stu-id="48db9-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR: \_ no \_ SITENAME**</span><span class="sxs-lookup"><span data-stu-id="48db9-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-570">1919 (0x77F)</span><span class="sxs-lookup"><span data-stu-id="48db9-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-571">No hay ningún nombre de sitio disponible para esta máquina.</span><span class="sxs-lookup"><span data-stu-id="48db9-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**no \_ se \_ puede obtener acceso al \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="48db9-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-573">1920 (0x780)</span><span class="sxs-lookup"><span data-stu-id="48db9-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-574">El sistema no puede tener acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="48db9-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR no se pudo \_ \_ resolver el nombre de \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="48db9-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-576">1921 (0x781)</span><span class="sxs-lookup"><span data-stu-id="48db9-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-577">El sistema no puede resolver el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="48db9-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**\_ \_ \_ no coinciden los tipos de entrada de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-579">1922 (0x782)</span><span class="sxs-lookup"><span data-stu-id="48db9-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-580">La entrada no es del tipo esperado.</span><span class="sxs-lookup"><span data-stu-id="48db9-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ no \_ todos los \_ obj \_ exportados**</span><span class="sxs-lookup"><span data-stu-id="48db9-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-582">1923 (0x783)</span><span class="sxs-lookup"><span data-stu-id="48db9-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-583">No se pudo exportar todo el UUID de objeto a la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="48db9-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_interfaz RPC \_ S \_ no \_ exportada**</span><span class="sxs-lookup"><span data-stu-id="48db9-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-585">1924 (0x784)</span><span class="sxs-lookup"><span data-stu-id="48db9-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-586">No se pudo exportar la interfaz a la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="48db9-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_no se \_ agregó el perfil \_ \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-588">1925 (0x785)</span><span class="sxs-lookup"><span data-stu-id="48db9-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-589">No se pudo agregar la entrada de perfil especificada.</span><span class="sxs-lookup"><span data-stu-id="48db9-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**no se agregó el ETL de RPC \_ S \_ PRF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-591">1926 (0x786)</span><span class="sxs-lookup"><span data-stu-id="48db9-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-592">No se pudo agregar el elemento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**\_no se \_ \_ \_ \_ quitó el ETL de RPC S PRF**</span><span class="sxs-lookup"><span data-stu-id="48db9-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-594">1927 (0x787)</span><span class="sxs-lookup"><span data-stu-id="48db9-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-595">No se pudo quitar el elemento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**\_no se \_ \_ \_ \_ ha agregado el GRP de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-597">1928 (0x788)</span><span class="sxs-lookup"><span data-stu-id="48db9-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-598">No se pudo agregar el elemento de grupo.</span><span class="sxs-lookup"><span data-stu-id="48db9-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**\_no se \_ \_ \_ \_ quitó el GRP de RPC S**</span><span class="sxs-lookup"><span data-stu-id="48db9-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-600">1929 (0x789)</span><span class="sxs-lookup"><span data-stu-id="48db9-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-601">No se pudo quitar el elemento de grupo.</span><span class="sxs-lookup"><span data-stu-id="48db9-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR en el \_ \_ controlador km \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="48db9-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-603">1930 (0x78A)</span><span class="sxs-lookup"><span data-stu-id="48db9-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-604">El controlador de impresora no es compatible con una directiva habilitada en el equipo que bloquea los controladores NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="48db9-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**el \_ contexto de error \_ expiró**</span><span class="sxs-lookup"><span data-stu-id="48db9-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-606">1931 (0x78B)</span><span class="sxs-lookup"><span data-stu-id="48db9-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-607">El contexto ha expirado y ya no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="48db9-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**se \_ \_ \_ \_ superó la cuota de confianza por usuario \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-609">1932 (0x78C)</span><span class="sxs-lookup"><span data-stu-id="48db9-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-610">Se ha superado la cuota de creación de confianza delegada del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="48db9-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR en la \_ \_ cuota de confianza de usuario \_ \_ \_ superada**</span><span class="sxs-lookup"><span data-stu-id="48db9-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-612">1933 (0x78D)</span><span class="sxs-lookup"><span data-stu-id="48db9-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-613">Se ha superado la cuota total de creación de confianza delegada.</span><span class="sxs-lookup"><span data-stu-id="48db9-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR \_ al \_ eliminar \_ la \_ cuota de confianza \_ de usuario**</span><span class="sxs-lookup"><span data-stu-id="48db9-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-615">1934 (0x78E)</span><span class="sxs-lookup"><span data-stu-id="48db9-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-616">Se ha superado la cuota de eliminación de confianza delegada del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="48db9-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR de ERROR de \_ autenticación del \_ Firewall \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-618">1935 (0x78F)</span><span class="sxs-lookup"><span data-stu-id="48db9-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-619">El equipo en el que está iniciando sesión está protegido por un firewall de autenticación.</span><span class="sxs-lookup"><span data-stu-id="48db9-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="48db9-620">La cuenta especificada no tiene permiso para autenticarse en el equipo.</span><span class="sxs-lookup"><span data-stu-id="48db9-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR \_ de \_ conexiones de impresión remotas \_ \_ bloqueadas**</span><span class="sxs-lookup"><span data-stu-id="48db9-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-622">1936 (0x790)</span><span class="sxs-lookup"><span data-stu-id="48db9-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-623">Las conexiones remotas al administrador de trabajos de impresión están bloqueadas por una directiva establecida en el equipo.</span><span class="sxs-lookup"><span data-stu-id="48db9-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR \_ NTLM \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="48db9-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-625">1937 (0x791)</span><span class="sxs-lookup"><span data-stu-id="48db9-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-626">Error de autenticación porque se ha deshabilitado la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="48db9-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR \_ de \_ cambio de contraseña \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="48db9-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-628">1938 (0x792)</span><span class="sxs-lookup"><span data-stu-id="48db9-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-629">Error de inicio de sesión: la Directiva EAS requiere que el usuario cambie su contraseña para poder realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="48db9-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR \_ de \_ formato de píxel no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-631">2000 (0x7D0)</span><span class="sxs-lookup"><span data-stu-id="48db9-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-632">El formato de píxel no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR \_ de \_ controlador incorrecto**</span><span class="sxs-lookup"><span data-stu-id="48db9-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-634">2001 (0x7D1)</span><span class="sxs-lookup"><span data-stu-id="48db9-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-635">El controlador especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR \_ de \_ estilo de ventana no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-637">2002 (0x7D2)</span><span class="sxs-lookup"><span data-stu-id="48db9-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-638">El estilo de ventana o el atributo de clase no es válido para esta operación.</span><span class="sxs-lookup"><span data-stu-id="48db9-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_no se \_ \_ admite el metarchivo de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-640">2003 (0x7D3)</span><span class="sxs-lookup"><span data-stu-id="48db9-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-641">No se admite la operación de metarchivo solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_no se \_ \_ admite la transformación de errores**</span><span class="sxs-lookup"><span data-stu-id="48db9-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-643">2004 (0x7D4)</span><span class="sxs-lookup"><span data-stu-id="48db9-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-644">No se admite la operación de transformación solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_no se \_ \_ admite el REcorte de errores**</span><span class="sxs-lookup"><span data-stu-id="48db9-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-646">2005 (0x7D5)</span><span class="sxs-lookup"><span data-stu-id="48db9-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-647">No se admite la operación de recorte solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR \_ de \_ CMM no válido**</span><span class="sxs-lookup"><span data-stu-id="48db9-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-649">2010 (0x7DA)</span><span class="sxs-lookup"><span data-stu-id="48db9-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-650">El módulo de administración del color especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR \_ de \_ perfil no válido**</span><span class="sxs-lookup"><span data-stu-id="48db9-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-652">2011 (0x7DB)</span><span class="sxs-lookup"><span data-stu-id="48db9-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-653">El perfil de color especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_ \_ no \_ se encontró la etiqueta de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-655">2012 (0x7DC)</span><span class="sxs-lookup"><span data-stu-id="48db9-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-656">No se encontró la etiqueta especificada.</span><span class="sxs-lookup"><span data-stu-id="48db9-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**etiqueta de ERROR \_ \_ no \_ presente**</span><span class="sxs-lookup"><span data-stu-id="48db9-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-658">2013 (0x7DD)</span><span class="sxs-lookup"><span data-stu-id="48db9-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-659">No existe una etiqueta necesaria.</span><span class="sxs-lookup"><span data-stu-id="48db9-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR \_ de \_ etiqueta duplicada**</span><span class="sxs-lookup"><span data-stu-id="48db9-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-661">2014 (0x7DE)</span><span class="sxs-lookup"><span data-stu-id="48db9-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-662">La etiqueta especificada ya está presente.</span><span class="sxs-lookup"><span data-stu-id="48db9-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_perfil \_ de error no \_ asociado con el \_ \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="48db9-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-664">2015 (0x7DF)</span><span class="sxs-lookup"><span data-stu-id="48db9-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-665">El perfil de color especificado no está asociado con el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_ \_ no \_ se encontró el perfil de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-667">2016 (0x7E0)</span><span class="sxs-lookup"><span data-stu-id="48db9-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-668">No se encontró el perfil de color especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR \_ COLORSPACE no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-670">2017 (0x7E1)</span><span class="sxs-lookup"><span data-stu-id="48db9-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-671">El espacio de colores especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR \_ ICM \_ no \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="48db9-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-673">2018 (0x7E2)</span><span class="sxs-lookup"><span data-stu-id="48db9-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-674">La administración del color de la imagen no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR al \_ eliminar \_ el \_ XForm ICM**</span><span class="sxs-lookup"><span data-stu-id="48db9-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-676">2019 (0x7E3)</span><span class="sxs-lookup"><span data-stu-id="48db9-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-677">Se produjo un error al eliminar la transformación de color.</span><span class="sxs-lookup"><span data-stu-id="48db9-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR \_ de \_ transformación no válida**</span><span class="sxs-lookup"><span data-stu-id="48db9-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-679">2020 (0x7E4)</span><span class="sxs-lookup"><span data-stu-id="48db9-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-680">La transformación de color especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="48db9-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR \_ de \_ coincidencia de COLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="48db9-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-682">2021 (0x7E5)</span><span class="sxs-lookup"><span data-stu-id="48db9-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-683">La transformación especificada no coincide con el espacio de colores del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="48db9-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR \_ de \_ COLORINDEX no válido**</span><span class="sxs-lookup"><span data-stu-id="48db9-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-685">2022 (0x7E6)</span><span class="sxs-lookup"><span data-stu-id="48db9-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-686">El índice de color con nombre especificado no está presente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="48db9-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**el perfil de ERROR no \_ \_ \_ \_ coincide con el \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="48db9-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-688">2023 (0x7E7)</span><span class="sxs-lookup"><span data-stu-id="48db9-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-689">El perfil especificado está pensado para un dispositivo de un tipo diferente al del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR al \_ conectar \_ otra \_ contraseña**</span><span class="sxs-lookup"><span data-stu-id="48db9-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-691">2108 (0x83C)</span><span class="sxs-lookup"><span data-stu-id="48db9-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-692">La conexión de red se realizó correctamente, pero se tenía que solicitar una contraseña distinta a la del usuario que se especificó originalmente.</span><span class="sxs-lookup"><span data-stu-id="48db9-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR de \_ conexión de \_ otra \_ contraseña \_ predeterminada**</span><span class="sxs-lookup"><span data-stu-id="48db9-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-694">2109 (0x83D)</span><span class="sxs-lookup"><span data-stu-id="48db9-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-695">La conexión de red se realizó correctamente con las credenciales predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="48db9-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR \_ de \_ nombre de usuario incorrecto**</span><span class="sxs-lookup"><span data-stu-id="48db9-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-697">2202 (0x89A)</span><span class="sxs-lookup"><span data-stu-id="48db9-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-698">El nombre de usuario especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="48db9-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR \_ no \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="48db9-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-700">2250 (0x8CA)</span><span class="sxs-lookup"><span data-stu-id="48db9-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-701">Esta conexión de red no existe.</span><span class="sxs-lookup"><span data-stu-id="48db9-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR al \_ abrir \_ archivos**</span><span class="sxs-lookup"><span data-stu-id="48db9-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-703">2401 (0x961)</span><span class="sxs-lookup"><span data-stu-id="48db9-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-704">Esta conexión de red tiene archivos abiertos o solicitudes pendientes.</span><span class="sxs-lookup"><span data-stu-id="48db9-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_conexiones activas de error \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-706">2402 (0x962)</span><span class="sxs-lookup"><span data-stu-id="48db9-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-707">Todavía existen conexiones activas.</span><span class="sxs-lookup"><span data-stu-id="48db9-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_dispositivo \_ de error en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="48db9-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-709">2404 (0x964)</span><span class="sxs-lookup"><span data-stu-id="48db9-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-710">El dispositivo está en uso por un proceso activo y no se puede desconectar.</span><span class="sxs-lookup"><span data-stu-id="48db9-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR \_ de \_ monitor de impresión desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-712">3000 (0xBB8)</span><span class="sxs-lookup"><span data-stu-id="48db9-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-713">Se desconoce el monitor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="48db9-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_ \_ controlador de impresora \_ de error en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="48db9-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-715">3001 (0xBB9)</span><span class="sxs-lookup"><span data-stu-id="48db9-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-716">El controlador de impresora especificado está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="48db9-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ no \_ se encontró el archivo de cola de errores**</span><span class="sxs-lookup"><span data-stu-id="48db9-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-718">3002 (0xBBA)</span><span class="sxs-lookup"><span data-stu-id="48db9-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-719">No se encontró el archivo de cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="48db9-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR \_ SPL \_ no \_ STARTDOC**</span><span class="sxs-lookup"><span data-stu-id="48db9-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-721">3003 (0xBBB)</span><span class="sxs-lookup"><span data-stu-id="48db9-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-722">No se emitió una llamada a StartDocPrinter.</span><span class="sxs-lookup"><span data-stu-id="48db9-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR \_ SPL \_ no \_ ADDJOB**</span><span class="sxs-lookup"><span data-stu-id="48db9-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-724">3004 (0xBBC)</span><span class="sxs-lookup"><span data-stu-id="48db9-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-725">No se emitió una llamada a AddJob.</span><span class="sxs-lookup"><span data-stu-id="48db9-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR en el \_ procesador de impresión \_ \_ ya \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="48db9-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-727">3005 (0xBBD)</span><span class="sxs-lookup"><span data-stu-id="48db9-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-728">El procesador de impresión especificado ya se ha instalado.</span><span class="sxs-lookup"><span data-stu-id="48db9-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**MONITOR de impresión de ERROR \_ \_ \_ ya \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="48db9-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-730">3006 (0xBBE)</span><span class="sxs-lookup"><span data-stu-id="48db9-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-731">El monitor de impresión especificado ya se ha instalado.</span><span class="sxs-lookup"><span data-stu-id="48db9-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR \_ de \_ monitor de impresión no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-733">3007 (0xBBF)</span><span class="sxs-lookup"><span data-stu-id="48db9-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-734">El monitor de impresión especificado no tiene las funciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="48db9-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR \_ \_ en el monitor \_ de impresión en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="48db9-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-736">3008 (0xBC0)</span><span class="sxs-lookup"><span data-stu-id="48db9-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-737">El monitor de impresión especificado está en uso actualmente.</span><span class="sxs-lookup"><span data-stu-id="48db9-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**la \_ impresora de error \_ tiene \_ trabajos \_ en cola**</span><span class="sxs-lookup"><span data-stu-id="48db9-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-739">3009 (0xBC1)</span><span class="sxs-lookup"><span data-stu-id="48db9-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-740">La operación solicitada no se permite cuando hay trabajos en cola en la impresora.</span><span class="sxs-lookup"><span data-stu-id="48db9-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR \_ de \_ reinicio correcto \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="48db9-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-742">3010 (0xBC2)</span><span class="sxs-lookup"><span data-stu-id="48db9-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-743">La operación solicitada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="48db9-743">The requested operation is successful.</span></span> <span data-ttu-id="48db9-744">Los cambios no serán efectivos hasta que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="48db9-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR \_ de \_ reinicio correcto \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="48db9-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-746">3011 (0xBC3)</span><span class="sxs-lookup"><span data-stu-id="48db9-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-747">La operación solicitada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="48db9-747">The requested operation is successful.</span></span> <span data-ttu-id="48db9-748">Los cambios no serán efectivos hasta que se reinicie el servicio.</span><span class="sxs-lookup"><span data-stu-id="48db9-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**\_ \_ no \_ se encontró la impresora de error**</span><span class="sxs-lookup"><span data-stu-id="48db9-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-750">3012 (0xBC4)</span><span class="sxs-lookup"><span data-stu-id="48db9-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-751">No se encontró ninguna impresora.</span><span class="sxs-lookup"><span data-stu-id="48db9-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**\_Advertencia de \_ controlador de impresora de error \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-753">3013 (0xBC5)</span><span class="sxs-lookup"><span data-stu-id="48db9-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-754">Se sabe que el controlador de impresora no es confiable.</span><span class="sxs-lookup"><span data-stu-id="48db9-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**controlador de impresora de ERROR \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="48db9-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-756">3014 (0xBC6)</span><span class="sxs-lookup"><span data-stu-id="48db9-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-757">Se sabe que el controlador de impresora daña el sistema.</span><span class="sxs-lookup"><span data-stu-id="48db9-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**\_ \_ \_ paquete \_ de controladores de impresora de error en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="48db9-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-759">3015 (0xBC7)</span><span class="sxs-lookup"><span data-stu-id="48db9-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-760">El paquete de controladores de impresora especificado está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="48db9-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encuentra el paquete de controladores principales**</span><span class="sxs-lookup"><span data-stu-id="48db9-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-762">3016 (0xBC8)</span><span class="sxs-lookup"><span data-stu-id="48db9-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-763">No se encuentra un paquete de controladores principales necesario para el paquete de controladores de impresora.</span><span class="sxs-lookup"><span data-stu-id="48db9-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR \_ de \_ reinicio \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="48db9-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-765">3017 (0xBC9)</span><span class="sxs-lookup"><span data-stu-id="48db9-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-766">Error en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-766">The requested operation failed.</span></span> <span data-ttu-id="48db9-767">Es necesario reiniciar el sistema para revertir los cambios realizados.</span><span class="sxs-lookup"><span data-stu-id="48db9-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR \_ de \_ reinicio \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="48db9-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-769">3018 (0xBCA)</span><span class="sxs-lookup"><span data-stu-id="48db9-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-770">Error en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="48db9-770">The requested operation failed.</span></span> <span data-ttu-id="48db9-771">Se inició un reinicio del sistema para revertir los cambios realizados.</span><span class="sxs-lookup"><span data-stu-id="48db9-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR \_ al \_ descargar el controlador de impresora \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-773">3019 (0xBCB)</span><span class="sxs-lookup"><span data-stu-id="48db9-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-774">No se encontró el controlador de impresora especificado en el sistema y debe descargarse.</span><span class="sxs-lookup"><span data-stu-id="48db9-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR \_ de \_ reinicio del trabajo de impresión \_ \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="48db9-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-776">3020 (0xBCC)</span><span class="sxs-lookup"><span data-stu-id="48db9-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-777">No se pudo imprimir el trabajo de impresión solicitado.</span><span class="sxs-lookup"><span data-stu-id="48db9-777">The requested print job has failed to print.</span></span> <span data-ttu-id="48db9-778">Una actualización del sistema de impresión requiere volver a enviar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="48db9-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR \_ de \_ \_ manifiesto de controlador de impresora no válido \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-780">3021 (0xBCD)</span><span class="sxs-lookup"><span data-stu-id="48db9-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-781">El controlador de impresora no contiene un manifiesto válido o contiene demasiados manifiestos.</span><span class="sxs-lookup"><span data-stu-id="48db9-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR \_ al \_ compartir la impresora \_**</span><span class="sxs-lookup"><span data-stu-id="48db9-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-783">3022 (0xBCE)</span><span class="sxs-lookup"><span data-stu-id="48db9-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-784">No se puede compartir la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="48db9-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**solicitud de ERROR en \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="48db9-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-786">3050 (0xBEA)</span><span class="sxs-lookup"><span data-stu-id="48db9-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-787">La operación se pausó.</span><span class="sxs-lookup"><span data-stu-id="48db9-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48db9-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR \_ \_ de reemisión de e/s \_ como \_ almacenado en caché**</span><span class="sxs-lookup"><span data-stu-id="48db9-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48db9-789">3950 (0xF6E)</span><span class="sxs-lookup"><span data-stu-id="48db9-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="48db9-790">Vuelva a emitir la operación especificada como una operación de e/s almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="48db9-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="48db9-791">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48db9-791">Requirements</span></span>



| <span data-ttu-id="48db9-792">Requisito</span><span class="sxs-lookup"><span data-stu-id="48db9-792">Requirement</span></span> | <span data-ttu-id="48db9-793">Value</span><span class="sxs-lookup"><span data-stu-id="48db9-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48db9-794">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48db9-794">Minimum supported client</span></span><br/> | <span data-ttu-id="48db9-795">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="48db9-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="48db9-796">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48db9-796">Minimum supported server</span></span><br/> | <span data-ttu-id="48db9-797">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="48db9-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48db9-798">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48db9-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="48db9-799"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="48db9-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48db9-800">Vea también</span><span class="sxs-lookup"><span data-stu-id="48db9-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48db9-801">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="48db9-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




