---
description: Recupera las opciones asociadas a un recurso compartido DDE que se encuentra en la lista de usuarios del servidor de recursos compartidos de confianza.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Función NDdeGetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666245"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="3f032-103">NDdeGetTrustedShare función)</span><span class="sxs-lookup"><span data-stu-id="3f032-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="3f032-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="3f032-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="3f032-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="3f032-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="3f032-106">Recupera las opciones asociadas a un recurso compartido DDE que se encuentra en la lista de recursos compartidos de confianza del usuario del servidor.</span><span class="sxs-lookup"><span data-stu-id="3f032-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f032-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f032-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="3f032-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f032-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f032-109">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f032-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f032-110">Nombre del servidor en el que reside el DSDM.</span><span class="sxs-lookup"><span data-stu-id="3f032-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="3f032-111">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f032-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f032-112">Nombre del recurso compartido cuyo estado de confianza se está consultando.</span><span class="sxs-lookup"><span data-stu-id="3f032-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="3f032-113">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3f032-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f032-114">*lpdwTrustOptions* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f032-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f032-115">Puntero a una variable que recibe las opciones de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f032-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="3f032-116">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3f032-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="3f032-117">Están disponibles las siguientes opciones de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f032-117">The following trust options are available.</span></span>



| <span data-ttu-id="3f032-118">Value</span><span class="sxs-lookup"><span data-stu-id="3f032-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="3f032-119">Significado</span><span class="sxs-lookup"><span data-stu-id="3f032-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="3f032-120"><dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="3f032-121">Máscara usada para obtener el valor que se usa para invalidar el estado de presentación del recurso compartido DDE, si \_ \_ se establece NDDE Trust cmd \_ Show.</span><span class="sxs-lookup"><span data-stu-id="3f032-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="3f032-122"><dt>**NDDE \_ CONFIAR en \_ cmd \_ Mostrar**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="3f032-123">Invalide el estado de la presentación especificado en el DSDM del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="3f032-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="3f032-124"><dt>**NDDE \_ \_Recurso compartido \_ de confianza del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="3f032-125">Quite el estado de confianza del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="3f032-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="3f032-126"><dt>**NDDE \_ 0x40000000L de inicio de \_ recurso \_ compartido de confianza**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3f032-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="3f032-127">Permita que un cliente se inicie en la aplicación si ya se está ejecutando en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f032-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="3f032-128"><dt>**NDDE \_ \_ \_ Inicio del recurso compartido de confianza**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="3f032-129">Permite que la aplicación se inicie en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f032-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="3f032-130">*lpdwShareModId0* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f032-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f032-131">Puntero a una variable que recibe la primera parte del identificador de modificación del recurso compartido de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f032-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="3f032-132">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3f032-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f032-133">*lpdwShareModId1* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f032-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f032-134">Puntero a una variable que recibe la segunda parte del identificador de modificación del recurso compartido de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f032-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="3f032-135">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3f032-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f032-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f032-136">Return value</span></span>

<span data-ttu-id="3f032-137">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="3f032-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="3f032-138">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="3f032-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f032-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f032-139">Remarks</span></span>

<span data-ttu-id="3f032-140">El identificador de modificación del recurso compartido de confianza refleja la versión del recurso compartido DDE en el DSDM en el momento en que se concedió inicialmente el estado de confianza al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="3f032-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="3f032-141">El identificador de modificación del recurso compartido de confianza se usa principalmente para quitar recursos compartidos de confianza obsoletos.</span><span class="sxs-lookup"><span data-stu-id="3f032-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="3f032-142">Sin embargo, no es necesario que el usuario quite los recursos compartidos de confianza obsoletos.</span><span class="sxs-lookup"><span data-stu-id="3f032-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="3f032-143">El agente DDE de red quita los recursos compartidos obsoletos en nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f032-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f032-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f032-144">Requirements</span></span>



| <span data-ttu-id="3f032-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f032-145">Requirement</span></span> | <span data-ttu-id="3f032-146">Value</span><span class="sxs-lookup"><span data-stu-id="3f032-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f032-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f032-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3f032-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3f032-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3f032-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f032-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3f032-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f032-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3f032-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f032-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f032-152"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f032-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f032-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f032-154"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f032-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f032-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f032-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f032-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f032-157">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="3f032-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3f032-158">**NDdeGetTrustedShareW** (Unicode) y **NDdeGetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3f032-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="3f032-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f032-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f032-160">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="3f032-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="3f032-161">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="3f032-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="3f032-162">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="3f032-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 




