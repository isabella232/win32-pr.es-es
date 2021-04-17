---
description: El mensaje SENDDIALOGINSTANCEDATA de la línea de TSPI \_ hace que TAPI llame a la \_ función PROVIDERGENERICDIALOGDATA de TUISPI en la dll de la interfaz de usuario asociada a htDlgInst, pasándole el bloque de parámetros al que apunta lpParams, de longitud de dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Mensaje de LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690976"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="3867b-103">Mensaje de línea \_ SENDDIALOGINSTANCEDATA</span><span class="sxs-lookup"><span data-stu-id="3867b-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="3867b-104">El mensaje **\_ SENDDIALOGINSTANCEDATA** de la línea de TSPI hace que TAPI llame a la función [**\_ PROVIDERGENERICDIALOGDATA de TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) en la dll de la interfaz de usuario asociada a *htDlgInst*, pasándole el bloque de parámetros al que apunta *lpParams*, de longitud de *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="3867b-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3867b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3867b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3867b-106">*htDlgInst*</span><span class="sxs-lookup"><span data-stu-id="3867b-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="3867b-107">HTAPIDIALOGINSTANCE que se devolvió al proveedor de servicios cuando la instancia del cuadro de diálogo se creó con la [**línea \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span><span class="sxs-lookup"><span data-stu-id="3867b-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="3867b-108">*lpParams*</span><span class="sxs-lookup"><span data-stu-id="3867b-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="3867b-109">Puntero a un bloque de parámetros específico del proveedor que se transmite a la función [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de la dll de la interfaz de usuario, cuyo tamaño se especifica en *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="3867b-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="3867b-110">Si este parámetro se establece en **null**, se trata de una solicitud para cerrar el cuadro de diálogo inmediatamente y limpiar (el archivo dll de la interfaz de usuario no debe invocar [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante esta limpieza).</span><span class="sxs-lookup"><span data-stu-id="3867b-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="3867b-111">*dwSize*</span><span class="sxs-lookup"><span data-stu-id="3867b-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3867b-112">Tamaño en bytes del bloque de parámetros que se va a transmitir al archivo DLL de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3867b-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3867b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3867b-113">Requirements</span></span>



| <span data-ttu-id="3867b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3867b-114">Requirement</span></span> | <span data-ttu-id="3867b-115">Value</span><span class="sxs-lookup"><span data-stu-id="3867b-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3867b-116">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3867b-116">TAPI version</span></span><br/> | <span data-ttu-id="3867b-117">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3867b-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3867b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3867b-118">Header</span></span><br/>       | <dl> <span data-ttu-id="3867b-119"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3867b-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3867b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3867b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3867b-121">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="3867b-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="3867b-122">**TUISPI \_ providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="3867b-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="3867b-123">**LÍNEA \_ CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="3867b-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

