---
description: Concede el estado de confianza de recurso compartido DDE especificado en el contexto de usuarios actual.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Función NDdeSetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539963"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="cff13-103">NDdeSetTrustedShare función)</span><span class="sxs-lookup"><span data-stu-id="cff13-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="cff13-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="cff13-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="cff13-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="cff13-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="cff13-106">Concede el estado de confianza del recurso compartido DDE especificado en el contexto del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="cff13-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff13-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cff13-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="cff13-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cff13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cff13-109">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cff13-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff13-110">Nombre del servidor cuyo DSDM se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="cff13-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="cff13-111">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cff13-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff13-112">Nombre del recurso compartido al que se va a conceder el estado de confianza.</span><span class="sxs-lookup"><span data-stu-id="cff13-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="cff13-113">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cff13-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cff13-114">*dwTrustOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cff13-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff13-115">Opciones que afectan al estado de confianza del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="cff13-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="cff13-116">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cff13-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="cff13-117">Opción</span><span class="sxs-lookup"><span data-stu-id="cff13-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="cff13-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cff13-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="cff13-119"><dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="cff13-120">Máscara usada para obtener el valor que se usa para invalidar el estado de presentación del recurso compartido DDE, si \_ \_ se establece NDDE Trust cmd \_ Show.</span><span class="sxs-lookup"><span data-stu-id="cff13-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="cff13-121"><dt>**NDDE \_ CONFIAR en \_ cmd \_ Mostrar**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="cff13-122">Invalide el estado de la presentación especificado en el DSDM del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="cff13-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="cff13-123"><dt>**NDDE \_ \_Recurso compartido \_ de confianza del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="cff13-124">Quite el estado de confianza del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="cff13-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="cff13-125"><dt>**NDDE \_ 0x40000000L de inicio de \_ recurso \_ compartido de confianza**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cff13-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="cff13-126">Permita que un cliente se inicie en la aplicación si ya se está ejecutando en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="cff13-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="cff13-127"><dt>**NDDE \_ \_ \_ Inicio del recurso compartido de confianza**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="cff13-128">Permite que la aplicación se inicie en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="cff13-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cff13-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cff13-129">Return value</span></span>

<span data-ttu-id="cff13-130">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="cff13-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="cff13-131">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="cff13-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cff13-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cff13-132">Remarks</span></span>

<span data-ttu-id="cff13-133">El recurso compartido DDE debe crearse primero con [**NDdeShareAdd**](nddeshareadd.md).</span><span class="sxs-lookup"><span data-stu-id="cff13-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="cff13-134">Si se llama a **NDdeSetTrustedShare** con *dwTrustOptions* establecido en cero, el recurso compartido de confianza pierde su estado de confianza.</span><span class="sxs-lookup"><span data-stu-id="cff13-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="cff13-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cff13-135">Requirements</span></span>



| <span data-ttu-id="cff13-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cff13-136">Requirement</span></span> | <span data-ttu-id="cff13-137">Value</span><span class="sxs-lookup"><span data-stu-id="cff13-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cff13-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cff13-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cff13-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cff13-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cff13-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cff13-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cff13-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cff13-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cff13-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cff13-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cff13-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="cff13-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cff13-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="cff13-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cff13-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cff13-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff13-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cff13-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="cff13-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="cff13-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cff13-149">**NDdeSetTrustedShareW** (Unicode) y **NDdeSetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cff13-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="cff13-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="cff13-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff13-151">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="cff13-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="cff13-152">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="cff13-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="cff13-153">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="cff13-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




