---
title: IMsTscAxEvents OnConfirmClose, método
description: Se llama cuando el cliente llama al método RequestClose de IMsRdpClient.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Método OnConfirmClose Servicios de Escritorio remoto
- Método OnConfirmClose Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151221"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="de287-106">IMsTscAxEvents:: OnConfirmClose (método)</span><span class="sxs-lookup"><span data-stu-id="de287-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="de287-107">Se llama cuando el cliente llama al método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) .</span><span class="sxs-lookup"><span data-stu-id="de287-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="de287-108">En respuesta a este evento, se debe solicitar al usuario que confirme el cierre de la conexión.</span><span class="sxs-lookup"><span data-stu-id="de287-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="de287-109">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="de287-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="de287-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de287-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="de287-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de287-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de287-112">*pfAllowClose* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="de287-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de287-113">Si **Variant \_ es true**, el valor predeterminado indica que el usuario desea cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="de287-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="de287-114">Si la **variante \_ es falsa**, indica que el usuario no desea cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="de287-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="de287-115">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="de287-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de287-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de287-116">Return value</span></span>

<span data-ttu-id="de287-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="de287-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de287-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de287-118">Remarks</span></span>

<span data-ttu-id="de287-119">Cuando una aplicación contenedora llama al método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) , este método devuelve un valor que indica si el contenedor debe esperar a que se produzca un evento **OnConfirmClose** antes de cerrar la conexión de control.</span><span class="sxs-lookup"><span data-stu-id="de287-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="de287-120">Si **RequestClose** devuelve **controlCloseWaitForEvents** y el usuario está conectado e iniciado sesión en su servicios de escritorio remoto sesión, se desencadena el evento **OnConfirmClose** .</span><span class="sxs-lookup"><span data-stu-id="de287-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="de287-121">En ese momento, la aplicación contenedora puede preguntar al usuario, preguntando si el usuario desea cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="de287-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="de287-122">Si el usuario desea cerrar la conexión, la aplicación debe establecer el parámetro *pfAllowClose* en **Variant \_ true** y continuar con el cierre de la conexión.</span><span class="sxs-lookup"><span data-stu-id="de287-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="de287-123">Si el usuario no desea cerrar, la aplicación debe establecer *pfAllowClose* en **Variant \_ false** y dejar la conexión abierta.</span><span class="sxs-lookup"><span data-stu-id="de287-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="de287-124">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="de287-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de287-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de287-125">Requirements</span></span>



| <span data-ttu-id="de287-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de287-126">Requirement</span></span> | <span data-ttu-id="de287-127">Value</span><span class="sxs-lookup"><span data-stu-id="de287-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de287-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de287-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de287-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de287-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="de287-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de287-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de287-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de287-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="de287-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de287-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="de287-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de287-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="de287-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de287-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de287-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de287-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="de287-136">IID</span><span class="sxs-lookup"><span data-stu-id="de287-136">IID</span></span><br/>                      | <span data-ttu-id="de287-137">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="de287-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="de287-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="de287-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de287-139">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="de287-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





