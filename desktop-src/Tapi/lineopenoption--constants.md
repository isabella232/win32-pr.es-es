---
description: Las \_ constantes LINEOPENOPTION muestran las opciones disponibles para abrir una línea.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes de LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680847"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="448d3-103">Constantes de LINEOPENOPTION \_</span><span class="sxs-lookup"><span data-stu-id="448d3-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="448d3-104">Las **\_ constantes LINEOPENOPTION** muestran las opciones disponibles para abrir una línea.</span><span class="sxs-lookup"><span data-stu-id="448d3-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="448d3-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**</span><span class="sxs-lookup"><span data-stu-id="448d3-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="448d3-106">La aplicación está dispuesta a controlar las solicitudes de otras aplicaciones que tienen la línea abierta.</span><span class="sxs-lookup"><span data-stu-id="448d3-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="448d3-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**</span><span class="sxs-lookup"><span data-stu-id="448d3-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="448d3-108">Se debe informar a la aplicación de las nuevas llamadas creadas en el dispositivo de línea solo si dichas llamadas aparecen en la dirección especificada en el miembro **dwAddressID** de la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) señalada por el parámetro *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="448d3-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="448d3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="448d3-109">Remarks</span></span>

<span data-ttu-id="448d3-110">Vea [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) para obtener más detalles sobre el funcionamiento de estas opciones.</span><span class="sxs-lookup"><span data-stu-id="448d3-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="448d3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="448d3-111">Requirements</span></span>



| <span data-ttu-id="448d3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="448d3-112">Requirement</span></span> | <span data-ttu-id="448d3-113">Value</span><span class="sxs-lookup"><span data-stu-id="448d3-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="448d3-114">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="448d3-114">TAPI version</span></span><br/> | <span data-ttu-id="448d3-115">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="448d3-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="448d3-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="448d3-116">Header</span></span><br/>       | <dl> <span data-ttu-id="448d3-117"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="448d3-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




