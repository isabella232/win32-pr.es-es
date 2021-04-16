---
description: Obtiene un identificador para el cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'IWiaAppErrorHandler:: GetWindow (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716057"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="93c97-103">IWiaAppErrorHandler:: GetWindow (método)</span><span class="sxs-lookup"><span data-stu-id="93c97-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="93c97-104">Obtiene un identificador para el cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93c97-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93c97-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="93c97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93c97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c97-107">*phwnd* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="93c97-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c97-108">Tipo: \**hWnd \** _</span><span class="sxs-lookup"><span data-stu-id="93c97-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="93c97-109">HWND usado por el controlador de errores de la aplicación, el controlador de errores del controlador y los cuadros de diálogo de mensajes de dispositivo predeterminados (error e informativo).</span><span class="sxs-lookup"><span data-stu-id="93c97-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="93c97-110">El valor de salida puede ser _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="93c97-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c97-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93c97-111">Return value</span></span>

<span data-ttu-id="93c97-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="93c97-112">Type: **HRESULT**</span></span>

<span data-ttu-id="93c97-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="93c97-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93c97-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93c97-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c97-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93c97-115">Remarks</span></span>

<span data-ttu-id="93c97-116">*phwnd* apunta a la ventana pasada en [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) por el proxy de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="93c97-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="93c97-117">Esta ventana debe ser válida mientras dure la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="93c97-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c97-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93c97-118">Requirements</span></span>



| <span data-ttu-id="93c97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c97-119">Requirement</span></span> | <span data-ttu-id="93c97-120">Value</span><span class="sxs-lookup"><span data-stu-id="93c97-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93c97-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93c97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93c97-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="93c97-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="93c97-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93c97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93c97-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="93c97-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93c97-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93c97-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c97-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c97-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="93c97-127">IDL</span><span class="sxs-lookup"><span data-stu-id="93c97-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93c97-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93c97-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="93c97-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93c97-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="93c97-130"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93c97-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




