---
title: IMsTscNonScriptable ResetPassword, método
description: Restablece todos los Estados de contraseña en el control ActiveX Escritorio remoto.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Método ResetPassword Servicios de Escritorio remoto
- Método ResetPassword Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Interfaz IMsTscNonScriptable Servicios de Escritorio remoto, método ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492773"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="8b153-106">IMsTscNonScriptable:: ResetPassword (método)</span><span class="sxs-lookup"><span data-stu-id="8b153-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="8b153-107">Restablece todos los Estados de contraseña en el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="8b153-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="8b153-108">Puede llamar a este método para borrar las contraseñas que se almacenan en cualquiera de los tres formatos admitidos: texto sin formato, codificado de forma portátil o binario (no portable).</span><span class="sxs-lookup"><span data-stu-id="8b153-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="8b153-109">Tenga en cuenta que las contraseñas codificadas no se deben considerar cifradas de forma segura.</span><span class="sxs-lookup"><span data-stu-id="8b153-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b153-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b153-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="8b153-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b153-111">Parameters</span></span>

<span data-ttu-id="8b153-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8b153-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b153-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b153-113">Return value</span></span>

<span data-ttu-id="8b153-114">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="8b153-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b153-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b153-115">Remarks</span></span>

<span data-ttu-id="8b153-116">Puede llamar a este método para restablecer la contraseña del control después de desconectarse.</span><span class="sxs-lookup"><span data-stu-id="8b153-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="8b153-117">Esto garantiza que las conexiones posteriores que utilicen la misma instancia del control no inicien sesión automáticamente con una contraseña establecida previamente.</span><span class="sxs-lookup"><span data-stu-id="8b153-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="8b153-118">Solo puede llamar a este método cuando el control ActiveX Escritorio remoto no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="8b153-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="8b153-119">Este método devuelve **E \_ FAIL** si se le llama cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="8b153-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="8b153-120">Para comprobar el estado de conexión, llame al método [**Get \_ Connected**](imstscax-connected.md) a través de la interfaz [**IMsTscAx**](imstscax-interface.md) o una de las interfaces que hereda de él.</span><span class="sxs-lookup"><span data-stu-id="8b153-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="8b153-121">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8b153-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b153-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b153-122">Requirements</span></span>



| <span data-ttu-id="8b153-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b153-123">Requirement</span></span> | <span data-ttu-id="8b153-124">Value</span><span class="sxs-lookup"><span data-stu-id="8b153-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b153-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b153-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8b153-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b153-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8b153-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b153-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8b153-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b153-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8b153-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8b153-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b153-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b153-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b153-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b153-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b153-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b153-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b153-133">IID</span><span class="sxs-lookup"><span data-stu-id="8b153-133">IID</span></span><br/>                      | <span data-ttu-id="8b153-134">IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="8b153-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b153-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b153-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b153-136">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="8b153-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





