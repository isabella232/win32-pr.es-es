---
description: El mensaje CREATEDIALOGINSTANCE de la línea \_ de TSPI hace que TAPI cree una asociación entre el proveedor de servicios y una instancia de la función providerGenericDialog de TUISPI que se \_ ejecuta en el contexto de la aplicación.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Mensaje de LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680180"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="3a88f-103">Mensaje de línea \_ CREATEDIALOGINSTANCE</span><span class="sxs-lookup"><span data-stu-id="3a88f-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="3a88f-104">El mensaje **\_ CREATEDIALOGINSTANCE** de la línea de TSPI hace que TAPI cree una asociación entre el proveedor de servicios y una instancia de la función [**\_ providerGenericDialog de TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) que se ejecuta en el contexto de la aplicación que invocó la función TSPI asincrónica identificada por el parámetro *dwRequestID* de la estructura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) a la que apunta *lpTUISPICreateDialogInstanceParams*.</span><span class="sxs-lookup"><span data-stu-id="3a88f-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3a88f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a88f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a88f-106">*hProvider*</span><span class="sxs-lookup"><span data-stu-id="3a88f-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="3a88f-107">ProviderHandle que se proporciona al proveedor de servicios como parámetro de [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span><span class="sxs-lookup"><span data-stu-id="3a88f-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="3a88f-108">*lpTUISPICreateDialogInstanceParams*</span><span class="sxs-lookup"><span data-stu-id="3a88f-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="3a88f-109">Puntero a una estructura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .</span><span class="sxs-lookup"><span data-stu-id="3a88f-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a88f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a88f-110">Requirements</span></span>



| <span data-ttu-id="3a88f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a88f-111">Requirement</span></span> | <span data-ttu-id="3a88f-112">Value</span><span class="sxs-lookup"><span data-stu-id="3a88f-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3a88f-113">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3a88f-113">TAPI version</span></span><br/> | <span data-ttu-id="3a88f-114">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3a88f-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3a88f-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a88f-115">Header</span></span><br/>       | <dl> <span data-ttu-id="3a88f-116"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a88f-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a88f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a88f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a88f-118">**TSPI \_ providerEnumDevices**</span><span class="sxs-lookup"><span data-stu-id="3a88f-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="3a88f-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="3a88f-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

